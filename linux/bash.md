# Bash - quick reference

## Contents

1. [Control operators](#control-operators)
1. [Redirection operators](#redirection-operators)
1. [Useful links](#useful-links)

## Control operators

| Operator | description |
| ---------| ----------- |
|;|Separate multiple commands on the same line|
|&|Execute command in the background|
|&&|logical AND. The second command is executed only if the first one succeeds.|
|&#124;&#124;|logical OR. The second command is executed only when the first command fails.|
|!|NOT operator|
|=~|Regex match|
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

## Useful links
1. [Bash How-to by SS64](https://ss64.com/bash/syntax.html)
1. [Linux Bash Shell Scripting Tutorial](https://bash.cyberciti.biz/guide/Main_Page)
1. [Bash Reference Manual](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html)
