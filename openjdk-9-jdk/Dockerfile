# NAME = openjdk
# TAGS = 9 9.0 9-ubuntu 9.0-ubuntu

# Pull base image.
FROM ubuntu:wily

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y openjdk-9-jdk && \
  rm -rf /var/lib/apt/lists/*

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-9-openjdk-amd64

# Define default command.
CMD ["bash"]
