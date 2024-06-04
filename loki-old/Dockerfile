FROM grafana/loki:2.0.0

RUN mkdir -p /etc/loki/rules-temp

COPY loki-config.yaml /etc/loki/loki-config.yaml
COPY rules /etc/loki/rules