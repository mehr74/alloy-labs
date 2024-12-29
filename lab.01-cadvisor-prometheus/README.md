# cAdvisor and Prometheus


![cAdvisor Metrics](../.assets/cadvisor.prometheus.drawio.svg)

In this lab, we will use cAdvisor and Prometheus to monitor the containerized applications.
The lab is based on `docker`.

## Prerequisites
- Docker

## Steps

Start cAdvisor, Prometheus and Grafana

```bash
docker compose up -d
```

Checkout the services 

| Service | URL |
| --- | --- |
| cAdvisor | [http://localhost:8080/containers/](http://localhost:8080/containers/) |
| Prometheus | [http://localhost:9090/](http://localhost:9090/) |
| Grafana | [http://localhost:3000/](http://localhost:3000/) |

![Servces demo](../.assets/cadvisor.prometheus.demo.drawio.svg)

## References
[Failed to get docker info in MacOS](https://github.com/google/cadvisor/issues/1565)