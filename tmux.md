# Tmux - quick reference

## Content
- [Commands](#selected-commands)
- [Config file](#config-file)
- [Useful links](#useful-links)

## Selected commands
| Command | description |
| ------- | ----------- |
| `tmux` | start new session |
| `tmux new -s SESSION` | start new named session |
| `tmux a -t SESSION` | attach to named session |
| `PREFIX d` | detach from session |
| `tmux kill-session -t SESSION` | kill session |
| `tmux rename SESSION`| rename session |
| `PREFIX c` | create window |
| `PREFIX &` | kill window |
| `PREFIX z` | toggle pane zoom |
| `PREFIX x` | kill pane |
| `PREFIX s` | list sessions in interactive mode |
| `PREFIX <0-9>` | change to window at specified index |
| `PREFIX '` | prompt for window index and change to that window |

## Config file
- [.tmux.conf](https://github.com/michalpytlos/dotfiles/blob/master/.tmux.conf)
- [Configuring tmux - wiki](https://github.com/tmux/tmux/wiki/Getting-Started#configuring-tmux)

## Useful links
- [Tmux wiki](https://github.com/tmux/tmux/wiki)
