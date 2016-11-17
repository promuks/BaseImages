FROM registry.access.redhat.com/rhel7.2

RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-8.noarch.rpm && \
	yum install -y --setopt=tsflags=nodocs --enablerepo rhel-7-server-optional-rpms --enablerepo rhel-7-server-rpms wget tar unzip bzip2 which 

LABEL io.k8s.description="Platform for building Angular applications with Npm , Bower and Grunt" \
      io.k8s.display-name="Tomcat builder 1.0" \
      io.openshift.expose-services="8080:http" \
      io.openshift.tags="builder,tomcat" \
	  io.openshift.s2i.scripts-url=image:///usr/local/sti

COPY scripts/ /usr/local/bin

# Set the default CMD for the image
CMD ["usage"]
