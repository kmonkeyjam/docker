FROM openjdk:8-jre

RUN /usr/bin/curl -L https://s3-us-west-2.amazonaws.com/dynamodb-local/dynamodb_local_latest.tar.gz | /bin/tar xz

ENTRYPOINT ["/usr/bin/java", "-Djava.library.path=./DynamoDBLocal_lib", "-jar", "DynamoDBLocal.jar"]

EXPOSE 10000

CMD ["-inMemory", "-port", "10000", "-sharedDb"]
