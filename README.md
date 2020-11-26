# MQTT-on-kubernetes

Config custom for HiveMQ Broker on Kuber

##  Install hivemq:
- Add repo HiveMQ:

`helm repo add helm repo add hivemq https://hivemq.github.io/helm-charts`

- Install HiveMQ broker with custom value:

`helm upgrade --install  hivemq hivemq/hivemq-operator --values values/value-hivemq.yaml -n hivemq`

- Install ingress-nginx with patch:

`helm upgrade --install ingress-nginx ingress-nginx/ingress-nginx -f hivemq/nginx-ingress-controller-config.yaml -n ingress-nginx`

- Install Prometheus and Grafana

`helm upgrade --install monitoring charts/monitoring --values values/value-hivemq.yaml -n monitoring`

## Reference:
- HiveMQ helm chart: https://github.com/hivemq/helm-charts
- Ingress for TCP: https://www.digitalocean.com/community/questions/can-ingress-proxy-be-enabled-and-disabled-for-individual-ports
- Apache Jmeter - mqtt plugin: https://github.com/xmeter-net/mqtt-jmeter

