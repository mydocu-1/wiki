# Wifi

## Service

```
# systemctl status wpa_supplicant@wlp4s0
```

## Connect

```
# wpa_supplicant -B -i wlp4s0 -c /etc/wpa_supplicant/example.conf
```

## Add connection

```
# vim /etc/wpa_supplicant-wlp4s0.conf
```

```
# wpa_passphrase MYSSID passphrase >> /etc/wpa_supplicant/example.conf
```

