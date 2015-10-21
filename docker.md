# Docker

Stop all container
``` bash
docker stop $(docker ps -a -q)
```

Remove all container
``` bash
docker rm $(docker ps -a -q)
```

Remove all images
``` bash
docker rmi -f $(docker images -a -q)
```
