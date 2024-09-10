FROM prom/prometheus:v2.33.5


ENV HOSTNAME=mon.domain.local

COPY prometheus.yml /etc/prometheus/prometheus.yml
COPY rules /etc/prometheus/rules
