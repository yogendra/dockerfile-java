# NAME = tomee
# TAGS = latest plus
FROM openjdk:jre-alpine

ARG version=7.0.2
ARG flavor=webprofile


ENV PATH /usr/local/tomee/bin:$PATH

RUN mkdir -p /usr/local/tomee

WORKDIR /usr/local/tomee

ADD http://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/$version/apache-tomee-$version-$flavor.tar.gz tomee.tar.gz

RUN set -x \
	&& tar -xzf tomee.tar.gz \
	&& mv apache-tomee-$flavor-$version/* /usr/local/tomee \
	&& rm -Rf apache-tomee-$flavor-$version \
	&& rm bin/*.bat \
	&& rm tomee.tar.gz*

EXPOSE 8080

EXPOSE 8009

CMD ["catalina.sh", "run"]

