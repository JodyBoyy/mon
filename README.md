# Taaghche Monitoring (ver 1.0.0)

full monitoring collection

## Features

1. prometheus for metrix collecting via exporters
2. log management for quering and labeling logs with Grafana Loki
3. grafana monitoring dashboard to show prometheus and Loki data

## Installation and Deployment

```
# clone. then pull repo and it's submodule

make update

# up and running

docker-compose up -d --build
```