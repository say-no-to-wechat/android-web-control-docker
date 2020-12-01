# Remote control android phone from web

## CURRENT STATUS: first version useable. many problems to solve. 

## tools chain

ADB + scrcpy + VNC server on Linux + web VNC

some scripts to make web interface better. 

## hacks

docker host should NOT run adb.

android: navbar app (https://play.google.com/store/apps/details?id=nu.nav.bar&hl=en_US&gl=US) or enable android built-in navbar (https://forum.xda-developers.com/chef-central/android/how-to-enable-navigation-bar-android-t3461012)

webVNC base: https://github.com/fcwu/docker-ubuntu-vnc-desktop

sudo docker run --privileged -v /dev/bus/usb:/dev/bus/usb -p 6080:80 -v /dev/shm:/dev/shm dorowu/ubuntu-desktop-lxde-vnc

TODO: self-adaptive resolution

