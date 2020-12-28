## Docker Monitoring 
- Run CAdvisor 

```
docker run \
  --volume=/:/rootfs:ro \
  --volume=/var/run:/var/run:rw \
  --volume=/sys:/sys:ro \
  --volume=/var/lib/docker/:/var/lib/docker:ro \
  --volume=/dev/disk/:/dev/disk:ro \
  --publish=8080:8080 \
  --detach=true \
  --name=cadvisor \
  google/cadvisor:latest
```
- With file system status with privilages 
```
sudo docker run   --volume=/:/rootfs:ro   --volume=/var/run:/var/run:ro   --volume=/sys:/sys:ro   --volume=/var/lib/docker/:/var/lib/docker:ro   --volume=/dev/disk/:/dev/disk:ro   --publish=8081:8080   --detach=true   --name=cadvisor2   --privileged   --device=/dev/kmsg   gcr.io/cadvisor/cadvisor:v0.36.0

```
- Cadvisor enables API Metrics : `http://localhost:8080/api/v1.3/docker ` and can access other paramertes by using parametes `containers,docker,events,machine,subcontainers`
