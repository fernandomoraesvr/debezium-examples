ARG STRIMZI_VERSION=latest-kafka-3.4.0
FROM quay.io/strimzi/kafka:${STRIMZI_VERSION}

ARG DEBEZIUM_CONNECTOR_VERSION=2.1.3.Final
ENV KAFKA_CONNECT_PLUGIN_PATH=/tmp/connect-plugins

RUN mkdir $KAFKA_CONNECT_PLUGIN_PATH &&\
    cd $KAFKA_CONNECT_PLUGIN_PATH &&\
    curl -sfSL https://repo1.maven.org/maven2/io/debezium/debezium-connector-mongodb/${DEBEZIUM_CONNECTOR_VERSION}/debezium-connector-mongodb-${DEBEZIUM_CONNECTOR_VERSION}-plugin.tar.gz | tar xz
