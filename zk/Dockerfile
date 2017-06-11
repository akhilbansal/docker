from faltuthingsido/openjre:8
RUN wget -q http://apache.mirrors.tds.net/zookeeper/stable/zookeeper-3.4.10.tar.gz
RUN tar -xzf zookeeper-3.4.10.tar.gz 
RUN mv zookeeper-3.4.10 zookeeper 
# RUN mv zookeeper/conf/zoo_sample.cfg zookeeper/conf/zoo.cfg 
EXPOSE 2181 2888 3888
WORKDIR /zookeeper
#ENTRYPOINT ["/zookeeper/bin/zkServer.sh"]