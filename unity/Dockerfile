FROM ghcr.io/linuxserver/baseimage-ubuntu:jammy

ARG DEBIAN_FRONTEND=noninteractive
ARG TMR_RELEASE=v1.0.1

RUN apt-get update && \
  apt-get install -y libglu1 libxcursor1 xvfb xz-utils && \
  curl -o \
    /tmp/TMR_Server.tar.xz -L \
    "https://github.com/DaRealRoyal/TacticalMathReturns/releases/download/${TMR_RELEASE}/TMR_Server.tar.xz" && \
  mkdir /app/tmr_server && \
  tar xf \
    /tmp/TMR_Server.tar.xz -C \
    /app/tmr_server --strip-components=1

COPY /root /
