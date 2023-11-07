# Arch installation on thinkPad X1 Carbon 5th gen

**F1** to enter BIOS:  disable secure boot<br>
**F12** to select USB as boot device

```
# lspci -k
```

## Setup wifi connection

```
# ip link set interface up
# wpa_supplicant -B -i interface -c <(wpa_passphrase MYSSID passphrase)
# dhcpd interface
# ping archlinux.org
```

```
# timedatectl set-ntp true
```

## Partition hard drive

```
# gdisk
```

260 MB for EF00 type of partition<br>
one partition for the rest

## Luks and LVM setup

```
# cryptsetup --key-size 512 --hash sha512 -y --use-random luksFormat /dev/nvme0n1p2
# cryptsetup luksOpen /dev/nvme0n1p2 luks
# pvcreate /dev/mapper/luks
# vgcreate vg0 /dev/mapper/luks
# lvcreate --size 16G vg0 --name swap
# lvcreate -l +100%FREE vg0 --name root
# mkfs.ext4 /dev/mapper/cryptroot
# mount /dev/mapper/cryptroot /mnt
# mkdir /mnt/boot
# mkfs.fat -F32 /dev/nvme0n1p1
# mount /dev/nvme0n1p1 /mnt/boot

# swapon /dev/mapper/vg0-swap
```

## System setup

```
# pacstrap /mnt base base-devel zsh vim git sudo efibootmgr iw wpa_supplicant dialog
```

```
# genfstab -pU /mnt >> /mnt/etc/fstab
```

Edit `/mnt/etc/fstab`
* On all non-boot partitions change to noatime (reduces wear if using an SSD)
* Add the following line tomake `/tmp` a ramdisk:
`tmpfs	/tmp	tmpfs	defaults,noatime,mode=1777	0	0`


```
# arch-chroot /mnt /bin/bash
```

```
# ln -s /usr/share/zoneinfo/America/Los_Angeles /etc/localtime
# hwclock --systohc --utcecho LANG=en_US.UTF-8 >> /etc/locale.conf
# echo LC_ALL= >> /etc/locale.conf
# echo MYHOSTNAME > /etc/hostname
```

Uncomment en-US.UTF-8 in `/etc/locale.gen` and generate locale

```
# locale-gen
# echo LANG=en_US.UTF-8 >> /etc/locale.conf
# echo LC_ALL= >> /etc/locale.conf
```

## Add user

```
# passwd

# useradd -m -g users -G wheel,storage -s /bin/zsh MYUSERNAME
# passwd MYUSERNAME
```

## Configure startup

Configure mkinitcpio:
* Add 'encrypt' and 'lvm2' to HOOKS before 'filesystems'
* Add 'resume' after 'lvm2' (also has to be after 'udev')

```
# mkinitcpio -p linux
```

```
# bootctl --path=/boot install
```

Append following lines to `/boot/loader/loader.conf`
* default arch
* timeout 5

Create `/boot/loader/entries/arch.conf` (use blkid to get UUID)

```
title Arch Linux
linux /vmlinuz-linux
initrd /initramfs-linux.img
options cryptdevice=UUID=<UUID>:vg0 root=/dev/mapper/vg0-root resume=/dev/mapper/vg0-swap rw acpi_backlight=video
```

## Complete setup and reboot

```
# exit
# umount -R /mnt
# swapoff -a
# reboot
```
