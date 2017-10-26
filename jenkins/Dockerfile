FROM jenkins
USER root

RUN apt-get update
RUN apt-get install -y apt-utils
RUN apt-get install -y sudo
RUN apt-get install -y wget
RUN apt-get install -y unzip

RUN wget https://services.gradle.org/distributions/gradle-3.2.1-bin.zip
RUN mkdir -p /usr/local/
RUN unzip -d /usr/local/ gradle-3.2.1-bin.zip 

USER jenkins

ENV PATH="/usr/local/gradle-3.2.1/bin:${PATH}"