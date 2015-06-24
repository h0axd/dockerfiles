FROM kalilinux/kali-linux-docker
MAINTAINER Tom Steele <tom@stacktitan.com>

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y metasploit-framework sudo build-essential
RUN cd /root && git clone https://github.com/Veil-Framework/Veil-Evasion.git && cd Veil-Evasion/setup && sed -e 's/kali/ubuntu/g' ./setup.sh > setup2.sh && chmod +x ./setup2.sh && ./setup2.sh --silent
