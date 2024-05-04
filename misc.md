# Miscellaneous

## Contents
* [Code review](#code-review)
* [Diagrams](#diagrams)
* [Effective speaking](#effective-speaking)
* [Kubernetes](#kubernetes)

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

