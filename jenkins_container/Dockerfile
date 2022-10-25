FROM centos:latest

RUN cd /etc/yum.repos.d/

RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*

RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

RUN yum install java-11-openjdk -y

RUN yum install wget -y

RUN yum install unzip -y

#RUN yum install tar -y

RUN yum install curl -y

RUN curl --silent --location http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo | tee /etc/yum.repos.d/jenkins.repo

RUN rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key

RUN yum install jenkins -y

#RUN systemctl start jenkins

#RUN systemctl status jenkins

#COPY wildfly1 /opt/.
#RUN mkdir /opt

#WORKDIR /opt

#RUN curl -O https://github.com/wildfly/wildfly/releases/download/26.1.2.Final/wildfly-26.1.2.Final.zip

#RUN unzip wildfly-26.1.2.Final.zip

#WORKDIR /opt/wildfly-26.1.2.Final/standalone/deployments/

#RUN curl -O -L https://github.com/AKSarav/SampleWebApp/raw/master/dist/SampleWebApp.war

EXPOSE 8080

#CMD ["systemctl", "enable", "jenkins"]

#CMD ["/opt/wildfly/bin/standalone.sh", "-b", "0.0.0.0"]
