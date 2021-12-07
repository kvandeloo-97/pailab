# pailab
Project repo for pailab rotation
## shell script to start netDx docker image
docker run -d --rm \
    -p 8787:8787 \
    -e PASSWORD=netdx \
    -v /u/kvandeloo/software:/software \
    -v /data/kvandeloo:/data \
    --name kv_netdx \
    realpailab/netdx
docker exec -it kv_netdx /bin/bash
