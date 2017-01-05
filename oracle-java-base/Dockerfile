FROM ubuntu:wily

ADD java.list /etc/apt/sources.list.d/java.list

# Install Java.
RUN \
  apt-key adv  --keyserver keyserver.ubuntu.com --recv-keys EEA14886 && \
  echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections