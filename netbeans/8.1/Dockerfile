FROM ifbaeunapolis/wildfly-mysql
MAINTAINER Huggo Oliveira "huggo.oliveira1@gmail.com"

USER root 
#instal unzip && axel && x11 serve Installation
RUN apt-get install unzip
RUN apt-get install -q -y axel 
RUN apt-get install -y xorg

#install git e maven
RUN apt-get update && apt-get install -y  git 
RUN apt-get install -y maven

#install netbeans
RUN axel http://download.netbeans.org/netbeans/8.1/final/zip/moduleclusters/netbeans-8.1-201510222201-all-in-one.zip
RUN unzip netbeans-8.1-201510222201-all-in-one.zip

#push project SADE IFBA Eunapolis-BA 
RUN mkdir /home/NetBeansProjects 
RUN cd /home/NetBeansProjects &&  git clone https://github.com/IFBAEunapolis/SADE.git 

CMD /netbeans/bin/netbeans
