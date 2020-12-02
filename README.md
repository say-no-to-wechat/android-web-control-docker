# Remote control android phone from web

## CURRENT STATUS: first version useable. many problems to solve. 

## toolchain

ADB + scrcpy + VNC server on Linux + web VNC

## Prepare your android

- Enable ADB, and trust the docker container

- Enable navbar on your android device. Use [android built-in navbar](https://forum.xda-developers.com/chef-central/android/how-to-enable-navigation-bar-android-t3461012) if possible, or use an [navbar app](https://play.google.com/store/apps/details?id=nu.nav.bar&hl=en_US&gl=US) .

- In developer settings, enable `stay awake`, to prevent android from sleeping. (If android went asleep, you can just close and re-run scrcpy)

- Set phone to minimal light level, to save power

## Prepare your server

- Plugin your android device by USB cable

- Run this program

```
sudo docker run --privileged -v /dev/bus/usb:/dev/bus/usb -p 6080:80 -v /dev/shm:/dev/shm -d --restart=always --name android-web docker.pkg.github.com/say-no-to-wechat/android-web-control-docker/android-web-control
```

- Use your way to access localhost:6080, run `fix-resolution.sh` in first login if necessary, and run `scrcpy` to connect.

## How to use web interface if you failed to enable navbar

- Desktop

Right-click for `back`, Middle-click for `home`, keyboard ctrl-S for `switch tasks`. 

- Mobile

Use noVNC tool on left side, to switch between `left-click`, `middle-click`, `right-click`. 

## Common mistake

The docker host should NOT run adb.

## TODO

self-adaptive resolution https://github.com/novnc/noVNC/issues/869

