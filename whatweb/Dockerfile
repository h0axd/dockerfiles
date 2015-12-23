FROM ruby:2.1.6
MAINTAINER Tom Steele <tom@stacktitan.com>

WORKDIR /root
RUN gem install json
RUN gem install bson
RUN gem install bson_ext
RUN gem install mongo

RUN git clone https://github.com/urbanadventurer/WhatWeb.git

WORKDIR /root/WhatWeb
RUN make install
