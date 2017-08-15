# smartworkx-postgres

## Create smartworkx-postgres in minikube

- cd kubernetes
- kubectl apply -f postgres-database.yml

## Example for running scripts against the postgres database

docker run -it --rm --volume=$(pwd):/scripts postgres psql -h 192.168.99.100 -p 30974 -U postgres -f scripts/create_db.sq