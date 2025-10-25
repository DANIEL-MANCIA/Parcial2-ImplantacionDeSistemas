# Parcial Docker Integrado

## Ejercicio 1 - Servicio Base con Dockerfile
### Comandos ejecutados:

- docker build -t parcial-api .
- docker run -d -p 3000:3000 --name parcial-container parcial-api

## Ejercicio 2 - Persistencia con PostgreSQL
### Comandos ejecutados:

- docker volume create db_data
- docker run -d --name postgres-db -e POSTGRES_USER=admin -e POSTGRES_PASSWORD=12345 -e POSTGRES_DB=parcial_db -v db_data:/var/lib/postgresql/data -p 5432:5432 postgres:15-alpine

## Ejercicio 3 - Docker Compose
### Comandos ejecutados:

- docker volume create db_data
- docker compose up -d --build

