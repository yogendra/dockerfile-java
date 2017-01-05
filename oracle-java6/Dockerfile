# NAME = java
# TAGS = 6 6.0 6-ubuntu 6.0-ubuntu

# Pull base image.
FROM yogendra/oracle-java-base:latest

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y oracle-java6-installer && \
  rm -rf /var/lib/apt/lists/* && \
  rm -rf /var/cache/oracle-jdk6-installer

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-6-oracle

# Define default command.
CMD ["bash"]
