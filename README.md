# prometheus, grafanas with otelp

- start example in /metrics
```
go run .
```

- start prometheus
```
docker run -d --name prometheus -p 9090:9090 -v <PATH_TO_prometheus.yml_FILE>:/etc/prometheus/prometheus.yml prom/prometheus --config.file=/etc/prometheus/prometheus.yml
```
1. `<PATH_TO_prometheus.yml_FILE>` in `/prometheus/promethus.yal`

- start grafana
```
docker run -d --name grafana -p 3000:3000 grafana/grafana
```
1. add first data source for prometheus http url `docker.for.mac.localhost:9090`
2. add new dashboard

## reference
https://medium.com/aeturnuminc/configure-prometheus-and-grafana-in-dockers-ff2a2b51aa1d