# wscef-docker 
## < trimmed repository readme from original >

[![Join the chat at https://gitter.im/farribeiro/wscef-docker](https://badges.gitter.im/farribeiro/wscef-docker.svg)](https://gitter.im/farribeiro/wscef-docker?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Warsaw in docker container. Warsaw is a security module, a.k.a Guardião, for brazilian
internet banking. This project is compatible of Banco do Brasil, Caixa Econômica
Federal and Sicredi.

## Pre-requisites

- Docker and Docker-Compose of your distro.
- Set BANKFILES variable (as `export BANKFILES=/home/ff/Downloads/Bankfiles`) to prevent volume creation error
- For transparency, privacy and security NEVER USE ANY PRE-BUILT DOCKER IMAGE FROM THIS PROJECT.
- Obtain a copy of the source code of this repository, check the content and build your own image.

## Instructions

Use docker compose to build and run the docker container, rather than `docker run`, 
since environments and volumes are set on `docker-compose.yml`.

**To build:** `docker-compose build wscef`

**To first run:** `docker-compose run --name wscef wscef`

**To other runs:** `docker start -i -a wscef`

**To purge everthing:** `docker-compose down --rmi all`, thanks[1]

**To force replace the container:** `docker-compose up --force-recreate`, thanks[1]
