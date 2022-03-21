FROM telegraf

RUN apt-get update
RUN apt-get install -y software-properties-common

RUN sed -i "/^# deb.*multiverse/ s/^# //" /etc/apt/sources.list
RUN sed -i "/^# deb.*universe/ s/^# //" /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y libsnmp-dev

RUN echo "deb http://ftp.de.debian.org/debian buster main non-free" >> /etc/apt/sources.list
RUn apt-get update
RUN apt-get install -y snmp-mibs-downloader
RUN download-mibs
