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
| `PREFIX w` | list windows in interactive mode |

## Config file
`.tmux.conf`
```
# Set prefix
set-option -g prefix C-a
unbind-key C-a
bind-key C-a send-prefix

# Use Alt-arrow keys to switch panes
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

# Use Shift-arrow to switch windows
bind -n S-Left previous-window
bind -n S-Right next-window

# Enable mouse mode
setw -g mouse on

# Split windows with h and v
bind-key v split-window -h
bind-key h split-window -v

# Hot-reload for config
bind-key r source-file ~/.tmux.conf \; display-message "~/.tmux.conf reloaded."

# Colours in terminal
# https://github.com/tmux/tmux/wiki/FAQ#how-do-i-use-a-256-colour-terminal
set -g default-terminal "screen-256color"

# Set colour of status bar and active pane border
set -g status-bg colour240
set -g pane-active-border-style bg=default,fg=colour240
```

## Useful links
- [Intro to tmux by Linode](https://www.linode.com/docs/guides/persistent-terminal-sessions-with-tmux/)
