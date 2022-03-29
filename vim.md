# Vim - quick reference

## Normal mode
| Command | description |
| ------- | ----------- |
| w | move to beginning of next word |
| e | move to end of current/next word |
| b | move to beginning of current/previous word |
| % | move to matching char. Default matchpairs: (), [], {} |
| `d ( d \| w \|  iw \| e \| b )` | delete/cut |
| dd | cut current line |
| dNd | cut N lines|
| dw | cut to beginning of next word |
| diw | cut entire word |
| de | cut to end of current word |
| db | cut from before cursor to beginning of word |
| D | cut to end of line |
| `c ( c \| w \| iw \| e \| b )` | change/replace |
| C | change to end of line |
| `y ( y \| w \| iw \| e \| b )` | yank/copy |
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
| ctrl + u | move cursor and screen up 1/2 page |
| ctrl + d | move cursor and screen down 1/2 page |
| u | undo last change |
| U | undo last changed line |
| ctrl + r | redo changes which were undone |
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

## Useful links
1. [Extensive Vim cheat sheet](https://vim.rtorr.com/)
2. [Vim setup for Python development](https://realpython.com/vim-and-python-a-match-made-in-heaven/)
