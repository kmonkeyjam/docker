FROM ubuntu:14.04

# Install prerequisites
RUN apt-get update
RUN apt-get install -y software-properties-common

# JAVA8
RUN /usr/bin/add-apt-repository ppa:webupd8team/java 2> /dev/null

# MISC
RUN apt-get -qq update
RUN mkdir -p /home/root/backuper/
RUN mkdir -p /tmp/
RUN /bin/echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections

### less frequent version changes
RUN apt-get install -qq -y tar unzip zip python-dateutil ant nginx git

# more frequent version changes
RUN apt-get install -qq -y oracle-java8-installer 
