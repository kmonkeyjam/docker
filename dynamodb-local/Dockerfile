FROM openjdk:8-jre

RUN /usr/bin/curl -L http://dynamodb-local.s3-website-us-west-2.amazonaws.com/dynamodb_local_latest | /bin/tar xz

ENTRYPOINT ["/usr/bin/java", "-Djava.library.path=./DynamoDBLocal_lib", "-jar", "DynamoDBLocal.jar"]

EXPOSE 8000

CMD ["-dbPath", "/var/dynamodb_local", "-port", "8000"]

VOLUME ["/var/dynamodb_local"]
