---
title: pgadmin docker
---

sudo docker run --name pgadmin -p 5050:80 -v /var/lib/pgadmin:/var/lib/pgadmin  -e 'PGADMIN_DEFAULT_EMAIL=email@no.com' -e 'PGADMIN_DEFAULT_PASSWORD=password' -d dpage/pgadmin4
