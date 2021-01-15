FROM ubuntu:18.04

RUN apt update
RUN apt install -y wget
RUN wget https://github.com/Motion-Project/motion/releases/download/release-4.3.2/bionic_motion_4.3.2-1_arm64.deb
RUN apt install -y ./bionic_motion_4.3.2-1_arm64.deb
RUN mkdir -p /usr/local/etc/motion/recordings /usr/local/etc/motion/conf/
CMD motion -c /usr/local/etc/motion/conf/motion.conf