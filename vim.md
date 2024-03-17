# Vim - quick reference

## Contents
1. [Normal mode](#normal-mode)
1. [Visual mode](#visual-mode)
1. [Insert mode](#insert-mode)
1. [Command-line mode](#command-line-mode)
1. [Windows](#windows)
1. [Marks](#marks)
1. [Tags](#tags)
1. [Macros](#macros)
1. [Neovim setup](#neovim-setup)
1. [Useful links](#useful-links)

## Normal mode

### Movement
| Command | description |
| ------- | ----------- |
| `f<char>` | move to next occurrence of char |
| `F<char>` | move to previous occurrence of char |
| `t<char>` | move to before next occurrence of char |
| `T<char>` | move to after previous occurrence of char |
| `;` | repeat last `f`, `t`, `F`, `T` command forward |
| `,` | repeat last `f`, `t`, `F`, `T` command backward |
| `w` | move to beginning of next word |
| `e` | move to end of current/next word |
| `b` | move to beginning of current/previous word |
| `%` | move to matching char. Default matchpairs: (), [], {} |
| `gg` | go to first line of document |
| `G` | go to last line of document |
| `<N>gg` | go to line N |
| `:<N>` | go to line N (is not jump)|
| `Ctrl + u` | move cursor and screen up 1/2 page |
| `Ctrl + d` | move cursor and screen down 1/2 page |

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
| * | search forward for word under cursor |
| # | search backward for word under cursor |
| >> | indent line |
| << | unindent line
| u | undo last change |
| U | undo last changed line |
| Ctrl + r | redo changes which were undone |
| . | repeat last command |
| za | toggle fold under cursor |

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
|Ctrl + n|Complete word|
|Ctrl + p|Complete word - back/previous|
| Ctrl + o | go to normal mode for just one command |
| Ctrl + Right Arrow | move to beginning of next word |
| Ctrl + Left Arrow | move to beginning of current/previous word |
| Ctrl + w | delete to beginning of current/previous word (to left of cursor) |
| Ctrl + u | delete everything to left of cursor |
| Ctrl + o D | delete everything to right of cursor |

## Command-line mode
| Command | description |
| ------- | ----------- |
| `:[range]g[lobal]/pattern/cmd`| Execute cmd on lines within range where pattern matches|
| `:%s/old/new/g` | Substitute. Search for `old` and replace with `new`.|
| `:%s/old/new/gc` | substitute with confirmations |
| `:g/pattern/d` | delete all lines that match pattern|
| `:v/pattenr/d` | delete all lines that do not match pattern|
| `/pattern` | search forward (downwards) for pattern |
| `?pattern` | search backward for pattern |
| `n` | next/repeat search in same direction |
| `N` | repeat search in opposite direction |
|`:set <option>?`|Display current value of option|
| `:reg` | view content of all registers |
| `:ju[mps]` | list jumps |
| `:ls` | list buffers |
| `:b <substring indentifying buffer>`|switch to buffer|
| `:bprev`| switch to previous buffer |
| `:bnext`| switch to next buffer |
| `:bd`| Unload buffer and delete from buffer list. Close all windows for this buffer. |
| `:bufdo bd` | unload all buffers |
| `:e` | reload current file |
| `:e <file>`| edit file |
| `:find <file>`|find file in path and then edit it|
| `:!<command>` | execute shell command |
| `%` | current file |
| `:qa` | quit all windows and quit vim |
| `wshada` | [neovim] write current state of shared data to shada file |
| `:so [<file>]` | execute commands from file |

## Windows
| Command | description |
| ------- | ----------- |
| `Ctrl + w (h\|j\|k\|l)` | move between windows |
| `Ctrl + w c` | Close current window |
| `Ctrl + w o` | Close other windows |
| `Ctrl + w v` | Vertical split |
| `Ctrl + w s` | Horizontal split |

## Marks
| Command | description |
| ------- | ----------- |
| `m<a-z>`| set buffer mark |
| `m<A-Z>`| set file mark |
| `'<mark>` | jump to mark |
| `:marks` | list marks |
| `:delm[arks] abxy` | delete marks a,b,x,y  |
| `:delm[arks]! ` | delete all lowercase marks for current buffer |

Uppercase marks are persistent and kept in the `main.shada` file. They are saved automatically on quiting vim.

## Tags
| Command | description |
| ------- | ----------- |
| `Ctrl + ]` | Jump to definition of keyword under cursor |
| `g Ctrl + ]` | Ambiguous tags. Display all tags for keyword under cursor and prompt for tag to jump to.|
| `Ctrl + t` | Jump back in tag stack|

To create tags file:
1. Ensure [universal-ctags](https://github.com/universal-ctags/ctags) is installed
1. Navigate to project root
1. Create tags file: `ctags -R --languages=python`

## Macros
| Command | description |
| ------- | ----------- |
| `q<a-z>` | record typed characters into register |
| `q` | stop recording |
| `@<a-z>` | execute content of register |
| `:g/pattern/norm! @a` | execute macro stored in register a on all lines matching pattern|
| `:5,10norm! @a`| execute on lines 5 through 10|

## Neovim setup
1. Install nvim from [snap](https://github.com/neovim/neovim-snap) or [AppImage](https://github.com/neovim/neovim/releases)
1. Install [vim-plug](https://github.com/junegunn/vim-plug#installation)
1. Copy [config files](https://github.com/michalpytlos/dotfiles/blob/master/nvim/) to `~/.config/nvim`
1. Install plugins: `:PlugInstall`

## Useful links
1. [Mastering the vim language - video](https://www.youtube.com/watch?v=wlR5gYd6um0)
1. [How to do 90% of what plugins do - video](https://www.youtube.com/watch?v=XA2WjJbmmoM)
