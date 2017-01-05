# NAME = openjdk
# TAGS = 6 6.0 6-ubuntu 6.0-ubuntu

# Pull base image.
FROM ubuntu:wily

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y openjdk-6-jdk && \
  rm -rf /var/lib/apt/lists/*

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-6-openjdk-amd64

# Define default command.
CMD ["bash"]
