FROM kalilinux/kali-linux-docker
MAINTAINER Tom Steele <tom@stacktitan.com>

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y metasploit-framework build-essential
WORKDIR /root
RUN git clone https://github.com/Veil-Framework/Veil-Evasion.git
WORKDIR /root/Veil-Evasion
RUN apt-get install -y xvfb moreutils
RUN echo "Xvfb :99 -screen 0 640x480x8 -nolisten tcp &" | cat - setup/setup.sh | head -n -1 |  sponge setup/setup.sh
RUN echo 'kill $(jobs -p) && exit 0' >> setup/setup.sh
ENV DISPLAY=:99
RUN bash setup/setup.sh -s
