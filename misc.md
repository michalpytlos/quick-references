# Miscellaneous

## Contents
* [Code review](#code-review)
* [Diagrams](#diagrams)
* [Effective speaking](#effective-speaking)
* [Kubernetes](#kubernetes)
* [WSL](#wsl)

## Code review
1. [Conventional Comments](https://conventionalcomments.org/) - standard for formatting review comments
1. [Code Review Developer Guide by Google](https://google.github.io/eng-practices/review/)

## Diagrams
1. [PlantUML reference](https://plantuml.com/) - diagrams as code
1. [Hitchhiker’s Guide to PlantUML](https://crashedmind.github.io/PlantUMLHitchhikersGuide/) - advanced PlantUML diagrams
1. [PlantUML color reference](https://plantuml-documentation.readthedocs.io/en/latest/formatting/color-names.html)

### VS Code setup for PlantUML
1. Create docker compose file to run [PlantUML server](https://plantuml.com/starting) locally.
2. Install [PlantUML](https://github.com/qjebbs/vscode-plantuml#readme) extension in VS Code.
3. [Configure the extension](https://github.com/qjebbs/vscode-plantuml#use-plantuml-server-as-render) to use the local server for rendering. 

`docker-compose.yml`
```yml
version: '3'

services:
  plantuml-server:
    image: plantuml/plantuml-server:jetty
    ports:
      - "8080:8080"
```
`.vscode/settings.json`
```json
{
	"plantuml.server": "http://localhost:8080",
	"plantuml.render": "PlantUMLServer"
}
```

## Effective speaking
1. [How to speak](https://www.youtube.com/watch?v=Unzc731iCUY) - Lecture by Patrick Winston

## Kubernetes
1. [kubectx](https://github.com/ahmetb/kubectx) - switch between contexts (clusters) on kubectl faster
1. [kubens](https://github.com/ahmetb/kubectx) - switch between namespaces on kubectl faster

## WSL

### Commands

| Command | description |
| ------- | ----------- |
| `wsl --shutdown` |Terminate all running distros and WSL |
| `wsl -l -v`|Show detailed info about all distros|
| `wsl -l -o`|List distros that can be installed|
| `wsl -d <distro>`|Run distro|
| `wsl -t <distro>`|Terminate/stop distro|
| `wsl --update`| Update WSL. See [release page](https://github.com/microsoft/WSL/releases) for changelog.|

### Configuration
* [wsl.conf](https://github.com/MicrosoftDocs/wsl/blob/main/WSL/wsl-config.md#wslconf)
* [.wslconfig](https://github.com/MicrosoftDocs/wsl/blob/main/WSL/wsl-config.md#wslconfig)

### Docker setup without Docker Desktop (Win 11 + Ubuntu 22.04):
#### PowerShell
1. Check if target Linux distro is running on WSL2: `wsl -l -v`
1. If WSL1, upgrade: `wsl --set-version <distro name> 2`

#### Linux distro
1. Switch to legacy iptables:
	* `sudo update-alternatives --set iptables /usr/sbin/iptables-legacy`
	* `sudo update-alternatives --set ip6tables /usr/sbin/ip6tables-legacy`
1. Install Docker: [docs](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)
1. (Optional) Manage Docker as non-root user: `sudo usermod -aG docker $USER` [docs](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user)

#### Windows 10
* Enable `systemd`: add to `/etc/wsl.conf`:
```
[boot]
systemd=true
```
* If there is no `systemd`, Docker daemon has to be run manually for Docker to work: `sudo dockerd`
