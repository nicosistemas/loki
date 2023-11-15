Crear ./loki-data-volumen para alojar datos
docker compose va a tomar los config tanto de loki como promtail

docker-compose -f docker-compose.yaml up -d


El resto de los yamls son para kubernetes aún en proyecto.

Test:

curl -v -H "Content-Type: application/json" -XPOST -s "http://localhost:3100/loki/api/v1/push" --data-raw \
 '{"streams": [{ "stream": { "foo": "bar2" }, "values": [ [ "1570818238000000000", "fizzbuzz" ] ] }]}'

fuente: 
- https://grafana.com/docs/loki/latest/installation/docker/
- https://volkovlabs.io/blog/nginx-loki-grafana-20230129/


Promtail:

Promtail instalado en windows (si, windowsssss :$ ) junto con su archivo de configuración promtail-local-config.yaml

.\promtail-windows-amd64.exe --config.file=promtail-local-config.yaml

- https://github.com/grafana/loki/releases
