# Docker - quick reference

## Selected CLI commands

### System
`docker system COMMAND`

| Command | description |
| ------- | ----------- |
| df | show docker disk usage |
| events | get real time events from |
| info | display system-wide info |
| prune | remove unused data |

### Containers
`docker container COMMAND`

#### Interact and inspect

| Command | description | usage |
| ------- | ----------- | ----- |
| attach | attach local stdin, stdout and stderr to running container ||
| cp | copy files/dirs between container and local filesystem ||
| diff | inspect changes to files/dirs on container's filesystem ||
| exec | run command in running container ||
|| set env vars | `-e, --env` |
|| keep stdin opened | `-i, --interactive` |
|| allocate pseudo-TTY | `-t, --tty` |
| inspect | display detailed info on one or more containers ||
| logs | fetch logs of container ||
|| follow log output | `-f, --follow` |
|| show n lines from tail | `-n, --tail` |
|| show timestamps |`-t, --timestamps`|
|| show logs since timestamp | `--since 2022-01-01T00:00:00Z` |
|| show logs before timestamp (42 minutes ago) |`--until 42m`|
| port | list port mappings for container ||
| stats | display live stream of container resource usage stats ||
| top | display running processes of container ||

#### Manage

| Command | description | usage |
| ------- | ----------- | ----- |
| create | create new container and prepare it to run specified command | `docker create [OPTIONS] IMAGE [COMMAND] [ARG...]` |
|| attach to stdin, stdout or stdout | `--attach ( STDIN \| STDOUT \| STDERR )` |
|| set env vars | `-e, --env` |
|| read in file of env vars | `--env-file` |
|| assign name to container | `--name` |
| rm | remove one or more containers ||
|| remove anonymous volumes associated with container | `-v, --volumes` |
| start | start one or more stopped containers ||
|| attach stdout/stderr and forward signals | `-a, --attach` |
|| attach container's stdin | `-i, --interactive` |
| stop | stop (SIGTERM) one or more running containers ||
| kill | kill (SIGKILL) one or more running containers ||
| run | create + start | `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]` |
|| run container in background | `-d, --detach` |

Other commands: `ls | prune | commit | pause | unpause | rename | restart | wait | update`

### Images
`docker image COMMAND`

| Command | description | usage |
| ------- | ----------- | ----- |
| build | build image from Dockerfile | `docker image build [OPTIONS] ( PATH \| URL \| - )`
|| do not use cache when building image | `--no-cache` |
|| name and optionally tag image | `--tag NAME:TAG` |
|| set target build stage | `--target BUILD_STAGE` |
| history | show history of image |
| pull | pull image or repo from registry |
| push | push image or repo to registry |
| tag | create tag that refers to source image | `docker image tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]` |

Other commands: `inspect | ls | prune | rm | save | load`

### Volumes
`docker volume ( create | inspect | ls | prune | rm )`

## docker-compose CLI commands