# NAME = java
# TAGS = 8 8.0 8-ubuntu 8.0-ubuntu

# Pull base image.
FROM yogendra/oracle-java-base:latest

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y oracle-java8-installer && \
  rm -rf /var/lib/apt/lists/* && \
  rm -rf /var/cache/oracle-jdk8-installer

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle

# Define default command.
CMD ["bash"]
