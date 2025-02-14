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

`<operator> [<count>] ( <motion> | <operator> )`

### Operators
| Command | description |
| ------- | ----------- |
|`c`|change|
|`d`|delete|
|`y`|yank into register|
|`~`|switch case (if `tildeop` is set)|
|`gu`|make lowercase|
|`gU`|make uppercase|
|`>`|shift right|
|`<`|shift left|
|`!<external command>`|filter through external command|
|`zf`|define fold|


### [Motions](https://neovim.io/doc/user/motion.html)
#### Left-right motions
| Command | description |
| ------- | ----------- |
|`0`|first char of line|
|`^`|first non-black char of line|
|`$`|end of line|
| `%` | move to matching char. Default matchpairs: (), [], {} |
| `f<char>` |next occurrence of char |
| `F<char>` |previous occurrence of char |
| `t<char>` |before next occurrence of char |
| `T<char>` |after previous occurrence of char |
| `;` | repeat last `f`, `t`, `F`, `T` command forward |
| `,` | repeat last `f`, `t`, `F`, `T` command backward |

#### Up-down motions
| Command | description |
| ------- | ----------- |
| `gg` | go to first line of document |
| `G` | go to last line of document |
| `<N>gg` | go to line N |
| `:<N>` | go to line N (is not jump)|
| `Ctrl + u` | move cursor and screen up 1/2 page |
| `Ctrl + d` | move cursor and screen down 1/2 page |

#### Word motions
| Command | description |
| ------- | ----------- |
| `w` |forward to beginning of word|
| `e` |forward to end of word|
| `b` |backward to beginning of word|
|`ge`|backward to end of word|
|`W \| E \| B \| gE`|same as lowercase motion but with [WORD](https://neovim.io/doc/user/motion.html#WORD)|

#### Text object motions
| Command | description |
| ------- | ----------- |
|`)`|sentence forward|
|`(`|sentence backward|
|`}`|paragraph forward|
|`{`|paragraph backward|
|`]]`|section/function forward|
|`[[`|section/function backward|

#### Text object selection
| Command | description |
| ------- | ----------- |
|`iw`|inner word|
|`iW`|inner WORD|
|`is`|inner sentence|
|`ip`|inner paragraph|
|`i]`|inner [] block|
|`i)`|inner () block|
|`i>`|inner <> block|
|`i}`|inner {} block|
|`i"`|inner quoted string|
|`i'`|inner quoted string|
|`a ( w \| W \| s \| p )`| same as inner version but with leading or trailing chars|
|`a ( ] \| ) \| > \| } \| " \| ' )`| same as inner version but with leading and trailing chars|

### Inserting
| Command | description |
| ------- | ----------- |
|`i`| insert before cursor |
|`a`| insert after cursor (append)|
|`I`| insert at beginning of line |
|`A`| insert at end of line (append)|
|`o`| open new line below current line |
|`O`| open new line above current line |

### Pasting
| Command | description |
| ------- | ----------- |
|`p`| paste after cursor |
|`P`| paste before cursor |
|`"xp`| paste content of register x |

### Other
| Command | description |
| ------- | ----------- |
|`*`| search forward for word under cursor |
|`#`| search backward for word under cursor |
|`u`| undo last change |
|`U`| undo last changed line |
|`Ctrl + r`| redo changes which were undone |
|`.`| repeat last command |
|`za`| toggle fold under cursor |
|`zz`| center screen on current line |
|`x`| cut char |
|`r`| replace char |
|`~`|switch case of char|
|`D`| cut to end of line |
|`C`| change to end of line |
|`Y`| yank to end of line |

## Visual mode
`<visual selection> <operator>`
| Command | description |
| ------- | ----------- |
| `o` | go to other end of selected text |
| `~ \| d \| c \| y \| > \| < \| !` | same as [here](#operators) |
|`u`| make lowercase |
|`U`| make uppercase |
| `<text object selection>` | same as [here](#text-object-selection) |

## Insert mode
| Command | description |
| ------- | ----------- |
|`Ctrl + n`|Complete word|
|`Ctrl + p`|Complete word - back/previous|
| `Ctrl + o` | go to normal mode for just one command |
| `Ctrl + Right Arrow` | move to beginning of next word |
| `Ctrl + Left Arrow` | move to beginning of current/previous word |
| `Ctrl + w` | delete to beginning of current/previous word (to left of cursor) |
| `Ctrl + u` | delete everything to left of cursor |
| `Ctrl + o D` | delete everything to right of cursor |

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
| `:wshada` | [neovim] write current state of shared data to shada file |
| `:so [<file>]` | execute commands from file |
| `:noh` | stop highlighting for hlsearch |
| `:set list` | show non-printing chars defined in listchars |
| `:w !<command>`|Execute command with highlighted text as `stdin`|
| `:r !command>`|Execute command and insert its `stdout` below cursor|


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
1. [Optional] Install chosen [Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/CascadiaMono#option-1-download-already-patched-font)
1. [Install nvim](https://github.com/neovim/neovim/blob/master/INSTALL.md#snap): `sudo snap install nvim --classic`
1. Install [vim-plug](https://github.com/junegunn/vim-plug#installation)
1. Copy config files to `~/.config/nvim`
1. Install plugins: `:PlugInstall`

## Useful links
1. [Mastering the vim language - video](https://www.youtube.com/watch?v=wlR5gYd6um0)
1. [How to do 90% of what plugins do - video](https://www.youtube.com/watch?v=XA2WjJbmmoM)
