---
title: pgadmin docker
---

## pgadmin
''''
sudo docker run --name pgadmin -p 5050:80 -v /home/nemorami/devel/pgadmin:/var/lib/pgadmin  -e "PGADMIN_DEFAULT_EMAIL=email@no.com "-e "PGADMIN_DEFAULT_PASSWORD=password" -d dpage/pgadmin4
''''
## agensgraph
''''
docker run -d     --name agensgraph     -e POSTGRES_PASSWORD=agens -p 5400:5432 -v /var/local/agens:/var/lib/postgresql/data docker.io/bitnine/agensgraph 
''''
