# Vim - quick reference

## Normal mode
| Command | description |
| ------- | ----------- |
| w | move to beginning of next word |
| e | move to end of current/next word |
| b | move to beginning of current/previous word |
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
| p | paste |
| "xp | paste content of register x |
| "+p | paste content of system clipboard |
| >> | indent line |
| >N> | indent N lines |
| << | unindent line
| N% | go to N percent of file |
| Ngg | go to line N |
| :N | go to line N |
| u | undo last operation |
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

## Command mode
| Command | description |
| ------- | ----------- |
| :reg | show content of all registers |
