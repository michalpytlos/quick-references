# Bash - quick reference

## Control operators

| Operator | description |
| ---------| ----------- |
|;|Separate multiple commands on the same line|
|&|Execute command in the background|
|&&|logical AND. The second command is executed only if the first one succeeds.|
|&#124;&#124;|logical OR. The second command is executed only when the first command fails.|
|!|NOT operator|
|&#124;&|Pass both std output and std error of one command as input to another|
|#|comment|

## Redirection operators

| Operator | description | example |
| ---------| ----------- | ------- |
|<|Pass input to command| command < in.txt |
|>|Direct std output of command into file|command > out.txt|
|2>|Direct std error of command into file| command > out.txt 2> error.txt|
|>>|Direct stdout of command into file. Append to the file.|command > out.txt|
|&>|Direct both stdout and stderr of command into file|command &> out_err.txt|
|&>>|Direct both stdout and stderr of command into file. Append to the file.|command &>> out_err.txt|
|<<|here document| https://bash.cyberciti.biz/guide/Here_documents|

## Shortcuts

| Shortcut | description |
| ---------| ----------- |
|alt + b|go back one word|
|alt + f|go forward one word|
|ctrl + w|cut word before cursor|
|ctrl + k|cut part of line after cursor|
|ctrl + u|cut part of line before cursor|
|ctrl + y|paste|
|ctrl + r|recall command|
|ctrl + z|suspend process|
|ctrl + d|close bash shell|
|ctrl + l|clear screen|
|ctrl + s|stop all output to screen|
|ctrl + q|resume output to screen|

## Useful links

1. [Linux Bash Shell Scripting Tutorial](https://bash.cyberciti.biz/guide/Main_Page)
2. [Bash Reference Manual](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html)
