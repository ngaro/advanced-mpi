FROM ubuntu:20.04
ARG TIMEZONE="Europe/Brussels"
RUN ln -s /usr/share/zoneinfo/$TIMEZONE /etc/localtime
RUN apt-get update && apt-get -y install build-essential libhdf5-openmpi-dev
ADD . /root
WORKDIR /root
RUN apt-get -y install libhdf5-openmpi-103
RUN h5pcc.openmpi hdf5.c
