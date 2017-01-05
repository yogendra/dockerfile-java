# NAME = java
# TAGS = 9 9.0 9-ubuntu 9.0-ubuntu

# Pull base image.
FROM yogendra/oracle-java-base:latest

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y oracle-java9-installer && \
  rm -rf /var/lib/apt/lists/* && \
  rm -rf /var/cache/oracle-jdk9-installer

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-9-oracle

# Define default command.
CMD ["bash"]
