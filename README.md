# Infraestructura Docker DEV - QA

## Descripción

Proyecto de infraestructura desarrollado utilizando Docker Compose.

Se implementan dos ambientes independientes:

- DEV
- QA

Cada ambiente cuenta con:

- Frontend con Nginx
- Backend con Node.js
- Base de datos PostgreSQL


## Arquitectura

Ambiente DEV:

Frontend:
Puerto 4001

Backend:
Puerto 4002

Base de datos:
Puerto 4003


Ambiente QA:

Frontend:
Puerto 5001

Backend:
Puerto 5002

Base de datos:
Puerto 5003


## Tecnologías utilizadas

- Docker Desktop
- Docker Compose
- Node.js
- Express
- Nginx
- PostgreSQL


## Estructura del proyecto

infraestructura-docker

backend/
- Dockerfile
- index.js
- package.json

frontend/
- Dockerfile
- index.html

docker-compose.yml

README.md


## Ejecución del proyecto

1. Clonar el repositorio:

git clone URL_DEL_REPOSITORIO


2. Ingresar a la carpeta del proyecto:

cd infraestructura-docker


3. Construir y ejecutar los servicios:

docker compose up -d --build


## Verificar contenedores

Ejecutar:

docker compose ps


## Servicios disponibles


DEV:

Frontend:
http://localhost:4001

Backend:
http://localhost:4002


QA:

Frontend:
http://localhost:5001

Backend:
http://localhost:5002


## Detener servicios

Para detener los contenedores:

docker compose down


## Volúmenes

Las bases de datos utilizan volúmenes Docker para mantener la persistencia:

- postgres_dev
- postgres_qa


## Conventional Commits

Los commits utilizados siguen la siguiente estructura:

feat: implementación de nuevas funcionalidades

fix: corrección de errores

docs: actualización de documentación


## Conclusión

La infraestructura permite ejecutar dos ambientes replicados mediante Docker Compose, facilitando la administración y despliegue de los servicios.