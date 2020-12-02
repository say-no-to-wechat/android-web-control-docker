# docker login https://docker.pkg.github.com -u GITHUB_UNAME --password-stdin
# docker build -f Dockerfile -t docker.pkg.github.com/say-no-to-wechat/android-web-control-docker/android-web-control .

FROM dorowu/ubuntu-desktop-lxde-vnc

RUN apt update && apt install -y scrcpy
COPY libfm.conf /root/.config/libfm/libfm.conf
COPY scrcpy.desktop /root/Desktop/scrcpy.desktop
COPY fix-resolution.sh /root/Desktop/fix-resolution.sh

