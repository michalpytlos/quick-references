# Docker CLI - quick reference

## Table of contents
- [System](#system)
- [Containers](#containers)
- [Images](#images)
- [Volumes](#volumes)
- [Misc](#misc)

## System
`docker system COMMAND`

| Command | description |
| ------- | ----------- |
| df | show docker disk usage |
| events | get real time events from server |
| info | display system-wide info |
| prune | remove unused data |

## Containers
`docker container COMMAND`

| Command | description | usage |
| ------- | ----------- | ----- |
| attach | attach local stdin, stdout and stderr to running container |`docker attach [OPTIONS] CONTAINER`|
| cp | copy files/dirs between container and local filesystem |`docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH \| docker cp [OPTIONS] SRC_PATH \|- CONTAINER:DEST_PATH`|
| diff | inspect changes to files/dirs on container's filesystem |`docker diff CONTAINER`|
| exec | run command in running container |`docker exec [OPTIONS] CONTAINER COMMAND [ARG...]`|
|| set env vars | `-e, --env` |
|| keep stdin opened | `-i, --interactive` |
|| allocate pseudo-TTY | `-t, --tty` |
| inspect | display detailed info on one or more containers |`docker container inspect [OPTIONS] CONTAINER [CONTAINER...]`|
| logs | fetch logs of container |`docker logs [OPTIONS] CONTAINER`|
|| follow log output | `-f, --follow` |
|| show n lines from tail | `-n, --tail` |
|| show timestamps |`-t, --timestamps`|
|| show logs since timestamp | `--since 2022-01-01T00:00:00Z` |
|| show logs before timestamp (42 minutes ago) |`--until 42m`|
| port | list port mappings for container |`docker port CONTAINER`|
| ps | list containers | `docker ps [OPTIONS]` |
| stats | display live stream of container resource usage stats |`docker stats [OPTIONS] [CONTAINER...]`|
| top | display running processes of container |`docker top CONTAINER [ps OPTIONS]`|

Manage commands: `create | rm | start | stop | kill | run | restart | pause | unpause | update | rename`

Other commands: `ls | prune | commit | wait`

## Images
`docker image COMMAND`

| Command | description | usage |
| ------- | ----------- | ----- |
| build | build image from Dockerfile | `docker image build [OPTIONS] ( PATH \| URL \| - )`
|| do not use cache when building image | `--no-cache` |
|| name and optionally tag image | `--tag NAME:TAG` |
|| set target build stage | `--target BUILD_STAGE` |
| history | show history of image |`docker history [OPTIONS] IMAGE`|
| pull | pull image or repo from registry |`docker pull [OPTIONS] NAME[:TAG\|@DIGEST]`|
| push | push image or repo to registry |`docker push [OPTIONS] NAME[:TAG]`|
| tag | create tag that refers to source image | `docker image tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]` |

Other commands: `inspect | ls | prune | rm | save | load`

## Volumes
`docker volume ( create | inspect | ls | prune | rm )`


## Misc

- [.dockerignore](https://docs.docker.com/engine/reference/builder/#dockerignore-file)