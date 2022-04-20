# Docker - quick reference

## Contents
- [Docker CLI](#docker-cli)
    - [System](#system)
    - [Containers](#containers)
    - [Images](#images)
    - [Volumes](#volumes)
- [Compose CLI](#compose-cli)
- [Useful links](#useful-links)


# Docker CLI
## System
`docker system COMMAND`

| Command | description | usage |
| ------- | ----------- | ----- |
| df | show docker disk usage | `docker sysytem df [OPTIONS]` |
||show detailed info on space usage|`-v, --verbose`|
| events | get real time events from server |`docker events [OPTIONS]`|
||filter output|`-f, --filter  FILTER*`|
||show events created since timestamp|`--since TIME_STRING*`|
||stream events until timestamp|`--until TIME_STRING*`|
| info | display system-wide info |`docker info`|
| prune | Remove unused containers, networks, images and, optionally, volumes |`docker system prune [OPTIONS]`|
||Remove all unused images not just dangling ones|`-a, --all`|
||Limit scope of prune|`--filter FILTER`|
||Also prune volumes|`--volumes`|

\* See [docs](https://docs.docker.com/engine/reference/commandline/system_events/#limiting-filtering-and-formatting-the-output) for more info on filtering and time-string formats.

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
| inspect | display detailed info on one or more containers |`docker inspect [OPTIONS] CONTAINER [CONTAINER...]`|
|| check if container is running |`docker inspect -f {{.State.Running}} CONTAINER`|
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

# Compose CLI

| Command | description | usage |
| ------- | ----------- | ----- |
| config | validate and view compose file ||
| build | build or rebuild services | `build [options] [--build-arg key=val...] [--] [SERVICE...]` |
|| do not use cache when bulding image | `--no-cache` |
| up | build, create, start and attach to containers for service|`up [options] [--scale SERVICE=NUM...] [--] [SERVICE...]`|
||detached mode|`-d, --detach`|
||recreate containers even if their conf and image haven't changed|`--recreate`|
||don't start services after creating them|`--no-start`|
||build images before starting containers|`--build`|
| down | stop containers and remove containers and networks (optionally also rm volumes and images) created by `up` |`down [options]`|
||remove images|`--rmi [all \| local]`|
||remove named volumes in compose and anonymous volumes attached to containers|`-v, --volumes`|
| images |list images used by created containers||
| events |receive real time events from containers||

Other manage commands: `rm | start | restart | stop | kill | pause | unpause`

Other commands: ` exec | logs | port | ps | run | top | pull | push`

# Useful links
- [.dockerignore](https://docs.docker.com/engine/reference/builder/#dockerignore-file)
- [Compose file reference](https://docs.docker.com/compose/compose-file/compose-file-v3/)
- [Multiple compose files](https://docs.docker.com/compose/extends/#multiple-compose-files)
