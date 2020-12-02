# docker login https://docker.pkg.github.com -u GITHUB_UNAME --password-stdin
# docker build -f Dockerfile -t docker.pkg.github.com/say-no-to-wechat/android-web-control-docker/android-web-control .
#
# Build this image in china got an error: apt can not find scrcpy. Please build this image in japan!

FROM dorowu/ubuntu-desktop-lxde-vnc

RUN apt update && apt install -y scrcpy
COPY libfm.conf /root/.config/libfm/libfm.conf
COPY scrcpy.desktop /root/Desktop/scrcpy.desktop
COPY fix-resolution.desktop /root/Desktop/fix-resolution.desktop

