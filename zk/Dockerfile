from akhil1980/jre:8
RUN wget http://apache.mirrors.tds.net/zookeeper/stable/zookeeper-3.4.10.tar.gz
RUN tar -xzf zookeeper-3.4.10.tar.gz 
RUN mv zookeeper-3.4.10 zookeeper 
#RUN mv zookeeper/conf/log4j.properties zookeeper/log4j.properties
#RUN mv zookeeper/conf zookeeper/_conf 

EXPOSE 2181 2888 3888
VOLUME /logDir
VOLUME /zookeeper/conf
VOLUME /dataDir


ENV ZOO_LOG4J_PROP="INFO,ROLLINGFILE"
ENV ZOO_LOG_DIR="/logDir" 
ENV ZOOCFGDIR="/zookeeper/conf"
WORKDIR /zookeeper

#ENTRYPOINT ["bin/zkServer.sh"]
#CMD ["start-foreground"]
CMD ["java","-cp","zookeeper-3.4.10.jar:lib/log4j-1.2.16.jar:lib/slf4j-log4j12-1.6.1.jar:lib/slf4j-api-1.6.1.jar:conf","org.apache.zookeeper.server.quorum.QuorumPeerMain","/zookeeper/conf/zoo.cfg"]

