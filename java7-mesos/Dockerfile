FROM java:7
MAINTAINER Dave Choi <goodoi09@gmail.com>

ARG MESOS_PKG
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF && \
echo "deb http://repos.mesosphere.io/debian jessie main" | tee /etc/apt/sources.list.d/mesosphere.list && \
apt-get update && \
apt-get install --no-install-recommends -y --force-yes mesos=$MESOS_PKG.debian81 && \
apt-get clean

ENV MESOS_NATIVE_JAVA_LIBRARY=/usr/local/lib/libmesos.so