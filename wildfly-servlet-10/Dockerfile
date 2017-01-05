# NAME = wildfly-servlet
# TAGS = 10 10.1 10.1.0 10.1.0.Final

FROM yogendra/java:8

# Set the WILDFLY_VERSION env variable
ENV WILDFLY_VERSION 10.1.0.Final
ENV WILDFLY_SHA1 26a7e38b67ba044d8bd6ba1bc5ffd7642fa497a1
ENV JBOSS_HOME /opt/jboss/wildfly


ADD https://jcenter.bintray.com/org/wildfly/wildfly-servlet-dist/10.1.0.Final/wildfly-servlet-dist-10.1.0.Final.tar.gz /tmp

RUN cd $HOME && \
    sha1sum /tmp/wildfly-servlet-dist-$WILDFLY_VERSION.tar.gz | grep $WILDFLY_SHA1 && \
    tar xf /tmp/wildfly-servlet-dist-$WILDFLY_VERSION.tar.gz && \
    mkdir -p "$(dirname "$JBOSS_HOME")" && \
    mv wildfly-servlet-$WILDFLY_VERSION $JBOSS_HOME && \
    rm /tmp/wildfly-servlet-dist-$WILDFLY_VERSION.tar.gz

# Ensure signals are forwarded to the JVM process correctly for graceful shutdown
ENV LAUNCH_JBOSS_IN_BACKGROUND true

WORKDIR $JBOSS_HOME

# Expose the ports we're interested in
EXPOSE 8080

# Set the default command to run on boot
# This will boot WildFly in the standalone mode and bind to all interface
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0"]
