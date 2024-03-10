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
| `tmux a` | attach to last active session |
| `tmux a -t SESSION` | attach to named session |
| `tmux kill-session -t SESSION` | kill session |
| `PREFIX d` | detach from session |
| `PREFIX c` | create window |
| `PREFIX &` | kill window |
| `PREFIX z` | toggle pane zoom |
| `PREFIX x` | kill pane |
| `PREFIX s` | list sessions in interactive mode |
| `PREFIX <0-9>` | change to window at specified index |
| `PREFIX '` | prompt for window index and change to that window |
| `PREFIX :` | prompt for command |
| `PREFIX ?` | list key bindings | 
| `PREFIX Ctrl-s` | Save tmux environment (tmux resurrect) |
| `PREFIX Ctrl-r` | Restore tmux environment (tmux resurrect) |

## Configuration
1. Clone [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm/blob/master/README.md#installation): `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
1. Create [~/.tmux.conf](https://github.com/michalpytlos/dotfiles/blob/master/.tmux.conf)
1. Start tmux: `tmux`
1. Fetch plugins: `PREFIX + I`

## Useful links
- [Configuring tmux - wiki](https://github.com/tmux/tmux/wiki/Getting-Started#configuring-tmux)
- [Tmux wiki](https://github.com/tmux/tmux/wiki)
- [List of tmux plugins](https://github.com/tmux-plugins/list)
