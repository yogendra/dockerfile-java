# NAME = openjdk
# TAGS = 9-jre 9.0-jre 9-jre-ubuntu 9.0-jre-ubuntu

# Pull base image.
FROM ubuntu:wily

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y openjdk-9-jre && \
  rm -rf /var/lib/apt/lists/*

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-9-openjdk-amd64

# Define default command.
CMD ["bash"]
