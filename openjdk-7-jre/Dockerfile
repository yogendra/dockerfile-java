# NAME = openjre
# TAGS = 7 7.0 7-ubuntu 7.0-ubuntu

# Pull base image.
FROM ubuntu:wily

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y openjdk-7-jre && \
  rm -rf /var/lib/apt/lists/*

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-7-openjdk-amd64

# Define default command.
CMD ["bash"]
