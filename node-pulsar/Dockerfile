FROM clevercloud/jnlp-agent-pulsar as pulsar

FROM jenkins/jnlp-agent-node

COPY --from=pulsar /usr/local/lib/libpulsar.so /usr/lib/libpulsar.so
COPY --from=pulsar /usr/local/lib/libpulsar.a /usr/lib/libpulsar.a
COPY --from=pulsar /usr/local/lib/libpulsarnossl.so /usr/lib/libpulsarnossl.a
COPY --from=pulsar /usr/local/include/pulsar /usr/include/pulsar

RUN apk -U add python3 make gcc g++

RUN npm install -g pulsar-client
