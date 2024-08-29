# Miscellaneous

## Contents
* [Code review](#code-review)
* [Diagrams](#diagrams)
* [Kubernetes](#kubernetes)
* [Github copilot](#github-copilot-in-vs-code)
* [Github actions](#github-actions)
* [Effective speaking](#effective-speaking)
* [Podcasts](#podcasts)

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

## Kubernetes
1. [kubectx](https://github.com/ahmetb/kubectx) - switch between contexts (clusters) on kubectl faster
1. [kubens](https://github.com/ahmetb/kubectx) - switch between namespaces on kubectl faster

## Github copilot in VS Code
* `Ctrl+Alt+I` - open chat view
* `Ctrl+Shift+I` - open quick chat
* [Chat participants doc](https://code.visualstudio.com/docs/copilot/copilot-chat#_chat-participants)
* [Slash commands doc](https://code.visualstudio.com/docs/copilot/copilot-chat#_slash-commands)
* [Chat variables doc](https://code.visualstudio.com/docs/copilot/copilot-chat#_use-chat-variables)

## Github Actions
* [Documentation](https://docs.github.com/en/actions)
* [Workflow Syntax](https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions)
* [Trigger events](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows)
* [Actions marketplace](https://github.com/marketplace?type=actions)

## Effective speaking
1. [How to speak](https://www.youtube.com/watch?v=Unzc731iCUY) - Lecture by Patrick Winston

## Podcasts
1. [Talk Python to Me](https://open.spotify.com/show/6Ol9sx1lONDxBSffLW9qcZ?si=e2a91948b9fb49bc&nd=1&dlsi=f14728e5d3084c30)
1. [Linux and Open Source News](https://open.spotify.com/show/3AZjRagzOkDX55Ftk8meuZ)
1. [Open Source Security Podcast](https://open.spotify.com/show/4YeKi2aGfxuhGj2QqazzVV)
1. [2.5 Admins](https://open.spotify.com/show/5SnfOIrOCRtTbCaDifDgjO)
