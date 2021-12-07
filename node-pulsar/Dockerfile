FROM clevercloud/jnlp-agent-pulsar as pulsar

FROM jenkins/jnlp-agent-node

COPY --from=pulsar /usr/lib/libpulsar.so /usr/lib/libpulsar.so
COPY --from=pulsar /usr/lib/libpulsar.a /usr/lib/libpulsar.a
COPY --from=pulsar /usr/lib/libpulsarwithdeps.a /usr/lib/libpulsarwithdeps.a
