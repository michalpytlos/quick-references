# Vim - quick reference

## Contents
1. [Normal mode](#normal-mode)
1. [Visual mode](#visual-mode)
1. [Insert mode](#insert-mode)
1. [Search and replace](#search-and-replace)
1. [Command mode](#command-mode)
1. [Neovim setup](#neovim-setup)
1. [Useful links](#useful-links)

## Normal mode
| Command | description |
| ------- | ----------- |
| w | move to beginning of next word |
| e | move to end of current/next word |
| b | move to beginning of current/previous word |
| % | move to matching char. Default matchpairs: (), [], {} |
| `d ( d \| w \| e \| b \| iw )` | delete/cut |
| dd | cut current line |
| dNd | cut N lines|
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
| >> | indent line |
| >N> | indent N lines |
| << | unindent line
| gg | go to first line of document |
| G | go to last line of document |
| Ngg | go to line N |
| :N | go to line N |
| N% | go to N percent of file |
| ggVG | select all |
| Ctrl + u | move cursor and screen up 1/2 page |
| Ctrl + d | move cursor and screen down 1/2 page |
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
| i | insert before cursor |
| I | insert at beginning of line |
| a | append/insert after cursor |
| A | append/insert at end of line |
| o | open new line below current line |
| O | open new line above current line |
| Ctrl + o | go to normal mode for just one command |
| Ctrl + Right Arrow | move to beginning of next word |
| Ctrl + Left Arrow | move to beginning of current/previous word |
| Ctrl + w | delete to beginning of current/previous word (to left of cursor) |
| Ctrl + u | delete everything to left of cursor |
| Ctrl + o D | delete everything to right of cursor |

## Search and replace
| Command | description |
| ------- | ----------- |
| /pattern | search for pattern |
| ?pattern | search backward for pattern |
| n | next/repeat search in same direction |
| N | repeat search in opposite direction |
| :%s/old/new/g | replace all old with new |
| :%s/old/new/gc | replace all old with new with confirmations |

## Command mode
| Command | description |
| ------- | ----------- |
| :reg | show content of all registers |

## Neovim setup
1. Install [vim-plug](https://github.com/junegunn/vim-plug#installation)
1. Create config file: `mkdir -p ~/.config/nvim && touch ~/.config/nvim/init.vim`
```vim
" Plugins
call plug#begin()

Plug 'joshdick/onedark.vim'
Plug 'tpope/vim-commentary'

call plug#end()

" Settings
syntax enable
colorscheme onedark
set number
set relativenumber

" Key mappings
nnoremap <C-_> :Commentary<CR>  " <C-_> is Ctrl + /
vnoremap <C-_> :Commentary<CR>

```
3. Install plugins: `:PlugInstall`


## Useful links
1. [Extensive Vim cheat sheet](https://vim.rtorr.com/)
