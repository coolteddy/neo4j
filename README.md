### Setup SSL Keypairs

```bash
openssl req -x509 -newkey rsa:4096 -keyout neo4j.key -out neo4j.crt -days 365 -nodes -subj "/CN=localhost"

coolteddy@coolteddy:~/DevOps/sandbox/Neo4j/certificates$ tree
.
├── bolt
│   ├── neo4j.crt
│   ├── neo4j.key
│   ├── revoked
│   └── trusted
│       └── neo4j.crt
├── https
│   ├── neo4j.crt
│   ├── neo4j.key
│   ├── revoked
│   └── trusted
│       └── neo4j.crt


coolteddy@coolteddy:~/DevOps/sandbox/Neo4j/certificates$ 

sudo chgrp -R 7474 certificates
sudo chgrp -R 7474 certificates

```