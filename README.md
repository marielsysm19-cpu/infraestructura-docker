# Infraestructura Docker DEV - QA

## Descripción

Este proyecto implementa una infraestructura utilizando Docker Compose.

La solución cuenta con dos ambientes independientes:

- DEV
- QA

Cada ambiente contiene los siguientes servicios:

- Frontend utilizando Nginx.
- Backend desarrollado con Node.js y Express.
- Base de datos PostgreSQL.

El objetivo es realizar una replicación de servicios mediante contenedores Docker para contar con ambientes separados de desarrollo y pruebas.


## Arquitectura

La infraestructura implementada es la siguiente:


## Ambiente DEV

Servicios:

- Frontend Nginx
  - Puerto: 4001

- Backend Node.js
  - Puerto: 4002

- Base de datos PostgreSQL
  - Puerto: 4003


## Ambiente QA

Servicios:

- Frontend Nginx
  - Puerto: 5001

- Backend Node.js
  - Puerto: 5002

- Base de datos PostgreSQL
  - Puerto: 5003


## Tecnologías utilizadas

- Docker Desktop
- Docker Compose
- Node.js
- Express
- Nginx
- PostgreSQL 17


## Estructura del proyecto

infraestructura-docker

backend
- Dockerfile
- index.js
- package.json

frontend
- Dockerfile
- index.html

docker-compose.yml

README.md


## Instalación y ejecución


### 1. Descargar el repositorio

Ejecutar:

git clone https://github.com/marielsysm19-cpu/infraestructura-docker.git


### 2. Ingresar al proyecto

Ejecutar:

cd infraestructura-docker


### 3. Construir y levantar los servicios

Ejecutar:

docker compose up -d --build


Este comando crea las imágenes Docker, redes, volúmenes y contenedores necesarios para ejecutar los ambientes DEV y QA.


## Verificación

Para verificar que los servicios estén funcionando:

docker compose ps


Servicios esperados:

DEV:

- web-dev
- api-dev
- bd-dev


QA:

- web-qa
- api-qa
- bd-qa


## Acceso a los servicios


### DEV

Frontend:

http://localhost:4001

Backend:

http://localhost:4002


### QA

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

Los cambios del proyecto utilizan la convención:

feat: implementación de nuevas funcionalidades

fix: corrección de errores

docs: actualización de documentación


Ejemplos:

feat: create docker infrastructure

docs: update README


## Conclusión

La infraestructura permite ejecutar dos ambientes replicados mediante Docker Compose.

Cada ambiente cuenta con frontend, backend y base de datos independientes, facilitando la administración y despliegue de servicios mediante contenedores Docker.