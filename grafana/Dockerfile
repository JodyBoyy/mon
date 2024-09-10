FROM grafana/grafana:latest

ENV HOSTNAME=mon.domain.local
ENV GF_DEFAULT_INSTANCE_NAME=mon.domain.local

ENV GF_SERVER_READ_TIMEOUT=1000s
ENV GF_USERS_ALLOW_SIGN_UP=false
ENV GF_DATAPROXY_TIMEOUT=90
RUN cd /var/lib/grafana && wget https://github.com/RedisGrafana/grafana-redis-datasource/releases/download/v2.2.0/redis-datasource-2.2.0.zip && \
  unzip redis-datasource-2.2.0.zip -d /var/lib/grafana/plugins/ && rm -rf redis-datasource-2.2.0.zip

RUN cd /var/lib/grafana && wget https://github.com/grafana/grafana-polystat-panel/releases/download/v2.1.11/grafana-polystat-panel-2.1.11.any.zip && \
  unzip grafana-polystat-panel-2.1.11.any.zip -d /var/lib/grafana/plugins/ && rm -rf grafana-polystat-panel-2.1.11.any.zip
