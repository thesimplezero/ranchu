# Docker Monitoring Stack

## Overview: 
  Docker Monitoring Stack utilizing Grafana, Prometheus, Node-Exporter, Redis and cAdvisor.

## Dependencies:
  - [Docker Compose](https://docs.docker.com/compose/install/linux/): Ensure either `docker-compose` or the `compose` plugin is installed.

## makefile:
  note: "Use the provided Makefile to detect your installed Docker Compose version."
  targets: "Run `make` to list available targets."

## How to boot:
  command: "`docker-compose up -d`"
  verification: "`docker-compose ps`"

## Endpoints

The following endpoints are available:

| Container      | Internal Endpoint         | External Endpoint     |
| -------------- | ------------------------- |---------------------- |
| Grafana        | http://grafana:3000       | http://localhost:3000 |
| Prometheus     | http://prometheus:9090    | http://localhost:9090 |
| Node-Exporter  | http://node-exporter:9100 | http://localhost:9100 |
| cAdvisor       | http://cadvisor:8080      | N/A                   |
| Alertmanager   | http://alertmanager:9093  | http://localhost:9093 |

## Cleanup

To remove the containers using docker compose (or `make clean`):

```bash
docker-compose down
```


