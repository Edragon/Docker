FROM python:2.7-stretch # debian stretch

RUN apt-get update && apt-get install -y \
    git \
    wget \
    make \
    grep \
    g++ \
  && apt-get clean


# Docker file
FROM python:2.7-stretch # debian + python 2.7
RUN apt-get update
RUN apt-get install gcc git wget make libncurses-dev flex bison gperf python python-serial -y
RUN apt-get clean

#enter into folder is not yet working now
#RUN mkdir -p ~/esp
#RUN cd ~/esp

# get the toolchain
RUN wget https://dl.espressif.com/dl/xtensa-lx106-elf-linux64-1.22.0-92-g8facf4c-5.2.0.tar.gz
RUN tar -xzf xtensa-lx106-elf-linux64-1.22.0-92-g8facf4c-5.2.0.tar.gz

# get the SDK
RUN git clone  https://github.com/espressif/ESP8266_RTOS_SDK.git

# export path
RUN export PATH="$PATH:/xtensa-lx106-elf/bin"
RUN export IDF_PATH=/ESP8266_RTOS_SDK