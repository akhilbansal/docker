from akhil1980/jre:8
RUN wget http://apache.mirrors.tds.net/zookeeper/stable/zookeeper-3.4.10.tar.gz
RUN tar -xzf zookeeper-3.4.10.tar.gz 
RUN mv zookeeper-3.4.10 zookeeper 
#RUN mv zookeeper/conf/log4j.properties zookeeper/log4j.properties
#RUN mv zookeeper/conf zookeeper/_conf 
COPY log4j.properties /zookeeper/
EXPOSE 2181 2888 3888
VOLUME /zookeeper/conf
VOLUME /dataDir
WORKDIR /zookeeper
ENTRYPOINT ["bin/zkServer.sh"]
CMD ["start-foreground"]
