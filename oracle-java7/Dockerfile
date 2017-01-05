# NAME = java
# TAGS = 7 7.0 7-ubuntu 7.0-ubuntu

# Pull base image.
FROM yogendra/oracle-java-base:latest

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y oracle-java7-installer && \
  rm -rf /var/lib/apt/lists/* && \
  rm -rf /var/cache/oracle-jdk7-installer

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-7-oracle

# Define default command.
CMD ["bash"]
