# NAME = wildfly-web
# TAGS = 10 10.1 10.1.0 10.1.0.Final

FROM yogendra/java:8

# Set the WILDFLY_VERSION env variable
ENV WILDFLY_VERSION 10.1.0.Final
ENV WILDFLY_SHA1 26a7e38b67ba044d8bd6ba1bc5ffd7642fa497a1
ENV JBOSS_HOME /opt/jboss/wildfly


RUN cd $HOME \
#    && curl -O https://download.jboss.org/wildfly/$WILDFLY_VERSION/wildfly-$WILDFLY_VERSION.tar.gz \
    && curl -O http://download.jboss.org/wildfly/$WILDFLY_VERSION/servlet/wildfly-servlet-$WILDFLY_VERSION.tar.gz
#    && sha1sum wildfly-$WILDFLY_VERSION.tar.gz | grep $WILDFLY_SHA1 \
    && tar xf wildfly-$WILDFLY_VERSION.tar.gz \
    && mv $HOME/wildfly-$WILDFLY_VERSION $JBOSS_HOME \
    && rm wildfly-$WILDFLY_VERSION.tar.gz

# Ensure signals are forwarded to the JVM process correctly for graceful shutdown
ENV LAUNCH_JBOSS_IN_BACKGROUND true

# Expose the ports we're interested in
EXPOSE 8080

# Set the default command to run on boot
# This will boot WildFly in the standalone mode and bind to all interface
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0"]