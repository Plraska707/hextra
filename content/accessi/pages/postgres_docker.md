---
title: PostgreSQL su Docker
type: docs
weight: 6
next: /
---

Per accedere al db PostgreSQL tramite docker, 
1. accedere al container del db con: `docker exec -it wikijs-db-1 /bin/bash`
2. accedere al db di postgresql con: `psql -U wikijs -d wiki`

Una volta nel db si possono usare i comandi SQL per interrogarlo, ad esempio

`SELECT * FROM users;`

fare attenzione al ; alla fine.
