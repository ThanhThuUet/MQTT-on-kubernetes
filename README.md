# MQTT-on-kubernetes

## Command:
- Install hivemq:

`helm upgrade --install  hivemq hivemq/hivemq-operator --values values/value-hivemq.yaml -n hivemq`

- Install ingress-nginx:

`helm upgrade --install ingress-nginx ingress-nginx/ingress-nginx -f hivemq/nginx-ingress-controller-config.yaml -n ingress-nginx`

## Reference:

- https://www.digitalocean.com/community/questions/can-ingress-proxy-be-enabled-and-disabled-for-individual-ports


