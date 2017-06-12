from akhil1980/kafka
# from akhil1980/alpinejdk:8
# RUN wget "http://apache.cs.utah.edu/kafka/0.8.2.2/kafka_2.10-0.8.2.2.tgz"
# RUN tar -xzf kafka_2.10-0.8.2.2.tgz
# RUN mv kafka_2.10-0.8.2.2 kafka
EXPOSE 9092
WORKDIR /kafka
ENTRYPOINT ["bin/kafka-server-start.sh"]
CMD ["config/server.properties"]