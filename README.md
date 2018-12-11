# Docker
Dockers for chaitanya R&amp;D

# Docker service DNS updates 
https://development.robinwinslow.uk/2016/06/23/fix-docker-networking-dns/

update in below location and reload/restart will fix the issue.


/etc/docker/daemon.json:
{
    "dns": ["10.0.0.2", "8.8.8.8"]
}
```
