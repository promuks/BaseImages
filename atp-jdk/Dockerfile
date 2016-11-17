FROM atp-rhel-utils

# Install build tools on top of base image
ENV JAVA_VERSION=8u45 BUILD_VERSION=b14 BUILDER_VERSION=1.0

# Downloading Java
RUN wget --no-cookies --no-check-certificate --header "Cookie: oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/$JAVA_VERSION-$BUILD_VERSION/jdk-$JAVA_VERSION-linux-x64.rpm" -O /tmp/jdk-8-linux-x64.rpm  && \
    yum -y --setopt=tsflags=nodocs install /tmp/jdk-8-linux-x64.rpm  && \
    yum clean all  && \
    rm  /tmp/jdk-8-linux-x64.rpm


COPY scripts/ /usr/local/bin
RUN chmod +x /usr/local/bin/usage
# Set the default CMD for the image
CMD ["usage"]
