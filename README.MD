Crear ./loki-data-volumen para alojar datos
docker compose va a tomar los config tanto de loki como promtail

docker-compose -f docker-compose.yaml up -d


El resto de los yamls son para kubernetes aún en proyecto.


fuente: 
- https://grafana.com/docs/loki/latest/installation/docker/
- https://volkovlabs.io/blog/nginx-loki-grafana-20230129/
