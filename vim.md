# Vim - quick reference

## Contents
1. [Normal mode](#normal-mode)
1. [Visual mode](#visual-mode)
1. [Insert mode](#insert-mode)
1. [Command-line mode](#command-line-mode)
1. [Neovim setup](#neovim-setup)

## Normal mode

### Movement
| Command | description |
| ------- | ----------- |
| `f<char>` | move to next occurrence of char |
| `F<char>` | move to previous occurrence of char |
| `;` | repeat last `f`, `t`, `F`, `T` command forward |
| `,` | repeat last `f`, `t`, `F`, `T` command backward |
| `w` | move to beginning of next word |
| `e` | move to end of current/next word |
| `b` | move to beginning of current/previous word |
| `%` | move to matching char. Default matchpairs: (), [], {} |
| `gg` | go to first line of document |
| `G` | go to last line of document |
| `<N>G` | go to line N |
| `:<N>` | go to line N (is not jump)|
| `Ctrl + u` | move cursor and screen up 1/2 page |
| `Ctrl + d` | move cursor and screen down 1/2 page |
| `Ctrl + o` | jump older |
| `Ctrl + i` | jump newer |

### Inserting
| Command | description |
| ------- | ----------- |
| i | insert before cursor |
| a | insert after cursor (append)|
| I | insert at beginning of line |
| A | insert at end of line (append)|
| o | open new line below current line |
| O | open new line above current line |

### Modify and copy
| Command | description |
| ------- | ----------- |
| `d ( d \| w \| e \| b \| iw )` | delete/cut |
| dd | cut current line |
| d\<N>d | cut N lines|
| dw | cut to beginning of next word (to right of cursor)|
| de | cut to end of current word (to right of cursor)|
| db | cut to beginning of current/previous word (to left of cursor)|
| diw | cut entire word |
| D | cut to end of line |
| `c ( c \| w \| e \| b \| iw )` | change/replace |
| C | change to end of line |
| `y ( y \| w \| e \| b \| iw )` | yank/copy |
| Y | yank to end of line |
| x | cut char |
| r | replace char |
| p | paste after cursor |
| P | paste before cursor |
| "xp | paste content of register x |
| "+p | paste content of system clipboard |
| "+y | yank to system clipboard |

### Other
| Command | description |
| ------- | ----------- |
| >> | indent line |
| >N> | indent N lines |
| << | unindent line
| u | undo last change |
| U | undo last changed line |
| Ctrl + r | redo changes which were undone |
| . | repeat last command |

## Visual mode
| Command | description |
| ------- | ----------- |
| d | cut |
| c | change |
| y | yank |
| > | indent |
| < | unindent |
| u | make lowercase |
| U | make uppercase |
| aw | mark word |

## Insert mode
| Command | description |
| ------- | ----------- |
| Ctrl + o | go to normal mode for just one command |
| Ctrl + Right Arrow | move to beginning of next word |
| Ctrl + Left Arrow | move to beginning of current/previous word |
| Ctrl + w | delete to beginning of current/previous word (to left of cursor) |
| Ctrl + u | delete everything to left of cursor |
| Ctrl + o D | delete everything to right of cursor |

## Command-line mode
| Command | description |
| ------- | ----------- |
| `:%s/old/new/gc` | substitute with confirmations |
| `:%s/old/new/g` | Substitute. Search for `old` and replace with `new`.|
| `:g/pattern/d` | delete all lines that match pattern|
| `:v/pattenr/d` | delete all lines that do not match pattern|
| `/pattern` | search forward (downwards) for pattern |
| `?pattern` | search backward for pattern |
| `n` | next/repeat search in same direction |
| `N` | repeat search in opposite direction |
| `:reg` | view content of all registers |
| `:ju[mps]` | view jump list |
| `:ls` | list buffers |
| `:b <buffer>` | switch to buffer |
| `:e <file>`| edit file |
| `:!<command>` | execute shell command |

## Neovim setup
1. Install [vim-plug](https://github.com/junegunn/vim-plug#installation)
1. Create config file: `mkdir -p ~/.config/nvim && touch ~/.config/nvim/init.vim`
```vim
" Plugins
call plug#begin()

Plug 'tpope/vim-commentary'
Plug 'tomasiser/vim-code-dark'
Plug 'folke/zen-mode.nvim'

call plug#end()

" Settings
syntax enable
colorscheme codedark
set number
set relativenumber

" Key mappings
nnoremap <C-_> :Commentary<CR>  " <C-_> is Ctrl + /
vnoremap <C-_> :Commentary<CR>
nnoremap <C-d> <C-d>zz
nnoremap <C-u> <C-u>zz


```
3. Install plugins: `:PlugInstall`
