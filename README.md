# smartworkx-postgres

## Create smartworkx-postgres in minikube

- cd kubernetes
- kubectl apply -f postgres-database.yml

## Example for running scripts against the postgres database

docker run -it --rm --volume=$(pwd):/scripts postgres psql -h 192.168.99.100 -p 30974 -U postgres -f scripts/create_db.sq

## Accessing postgres from gce needs a proxy:

- https://cloud.google.com/sql/docs/postgres/connect-container-engine
- Service account json stored in the repo (not checked in)
- Proxy password stored in keepass file
- INSTANCE_CONNECTION_NAME = smartworkx-173909:europe-west1:smartworkx
- 

