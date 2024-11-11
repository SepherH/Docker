grafana uses user 472, use the command to modify the grafana folder to 472:0 (grahana:root group)

chown 472:0 -Rv /volume1/docker/grafana/grafana/

command check loki uid
docker run --rm --entrypoint="" grafana/loki id
result
uid=10001(loki) gid=10001(loki) groups=10001(loki)
so. use the command to modify the loki folder to 10001:0
chown 10001:0 -Rv /volume1/docker/grafana/loki/