from akhil1980/jre:8

RUN wget http://apache.cs.utah.edu/zookeeper/zookeeper-3.4.10/zookeeper-3.4.10.tar.gz 
#COPY zookeeper-3.4.10.tar.gz / 
RUN tar -xzf zookeeper-3.4.10.tar.gz 
RUN rm zookeeper-3.4.10.tar.gz 
RUN mv zookeeper-3.4.10 zookeeper 

EXPOSE 2181 2888 3888

VOLUME ["/logDir","/zookeeper/conf","/dataDir"]

ENV ZOO_LOG4J_PROP="INFO,ROLLINGFILE" ZOO_LOG_DIR="/logDir" ZOOCFGDIR="/zookeeper/conf"

WORKDIR /zookeeper

#ENTRYPOINT ["bin/zkServer.sh"]
#CMD ["start-foreground"]

CMD ["java","-cp","zookeeper-3.4.10.jar:lib/log4j-1.2.16.jar:lib/slf4j-log4j12-1.6.1.jar:lib/slf4j-api-1.6.1.jar:conf","org.apache.zookeeper.server.quorum.QuorumPeerMain","/zookeeper/conf/zoo.cfg"]

