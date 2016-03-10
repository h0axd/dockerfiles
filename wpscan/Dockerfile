FROM ruby:2.1.8
MAINTAINER Tom Steele <tom@stacktitan.com>

WORKDIR /root
RUN apt-get install -y libcurl4-openssl-dev make zlib1g-dev
RUN git clone https://github.com/wpscanteam/wpscan.git
WORKDIR /root/wpscan
RUN bundle install --without test
