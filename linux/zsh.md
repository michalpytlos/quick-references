# Zsh - quick reference

## Contents

1. [Shortcuts](#shortcuts)
1. [Configuration](#configuration)
1. [Useful links](#useful-links)

## Shortcuts

Get a list of active key bindings: `bindkey`

### Insert mode in `vi-mode`
| Shortcut | description |
| ---------| ----------- |
|Ctrl + a|beginning of line|
|Ctrl + d|list choices|
|Ctrl + e|end of line|
|Ctrl + l|clear screen|
|Ctrl + r|reverse i search|
|Ctrl + u|kill line|
|Ctrl + v|paste from clipboard|
|Ctrl + w|backward kill word|

### Cross-shell
| Shortcut | description |
| ---------| ----------- |
|Ctrl + c|interrupt (SIGINT)|
|Ctrl + z|suspend and move to background (SIGTSTP)|
|Ctrl + s|stop all output to screen|
|Ctrl + q|resume output to screen|
|Ctrl + d|close shell|

## Configuration
1. Install Zsh:
    * `apt update`
    * `apt install zsh -y`
1. Set Zsh as the default shell: `chsh -s $(which zsh)`
1. [Install oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh#basic-installation)
1. [Install powerlevel10k](https://github.com/romkatv/powerlevel10k#oh-my-zsh)
1. Restart Zsh: `exec zsh`
1. [Enable vi-mode plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/vi-mode#vi-mode-plugin)

## Useful links
1. [Mastering Zsh - tutorial](https://github.com/rothgar/mastering-zsh)
1. [Zsh expansion guide](https://thevaluable.dev/zsh-expansion-guide-example/)
1. [Zsh completion guide](https://thevaluable.dev/zsh-completion-guide-examples/)