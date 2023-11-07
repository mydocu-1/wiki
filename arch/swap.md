# Swap file

To create 1GB swap file:

```
# fallocate -l 1G /swapfile1
# mkswap /swapfile1
# swapon /swapfile1
```

Add entry to `/etc/fstab` file:

```
/swapfile1 swap swap defaults 0 0
```

## Check if swap is activated or not

```
# free -m
```
