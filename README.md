# Linux - quick reference

List of common linux commands, operators and shortcuts with descriptions. The list is not meant to be exhaustive but rather serve as a quick reference for the author.


## Commands

| command | usage | description | more info | tags |
| --------| ----- |------------ | --------- | ---- |
|whatis|whatis <command\>|display one-line manual page descriptions||[discover]|


## Shell operators

### Control operators
| Operator | description |
| ---------| ----------- |
|;|Separate multiple commands on the same line|
|&|Execute command in the background|
|&&|logical AND. The second command is executed only if the first one succeeds.|
|&#124;&#124;|logical OR. The second command is executed only when the first command fails.|
|!|NOT operator|
|&#124;&|Pass both std output and std error of one command as input to another|
|#|comment|

### Redirection operators

| Operator | description | example |
| ---------| ----------- | ------- |
|<|Pass input to command| command < in.txt |
|>|Direct std output of command into file|command > out.txt|
|2>|Direct std error of command into file| command > out.txt 2> error.txt|
|>>|Direct std out of command into file. Append to the file.|command > out.txt|
|&>|Direct both std out and std err of command into file|command &> out_err.txt|
|&>>|Direct both std out and std err of command into file. Append to the file.|command &>> out_err.txt|
|<<|here document. See https://bash.cyberciti.biz/guide/Here_documents for more info|||

References:
1. http://linux-training.be/funhtml/ch13.html
2. https://unix.stackexchange.com/questions/159513/what-are-the-shells-control-and-redirection-operators


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

References:
1. https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/


## Files

To get information on the purpose of the typical default Linux directories run: `man hier`

| file | description | more info |
| -----| ----------- | --------- |
| /etc/services | file mapping services to port numbers ||
| /etc/passwd | user account info |https://www.cyberciti.biz/faq/understanding-etcpasswd-file-format/ |
| /etc/group | group account info ||
| /etc/sudoers | sudoers file - list of who can run what |https://www.sudo.ws/man/1.8.15/sudoers.man.html|


## Closer look at selected tools/commands


## Bibliography

1. https://explainshell.com/
2. https://www.howtoforge.com/linux-commands/
3. https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/
4. https://en.wikibooks.org/wiki/Linux_Guide
5. https://linuxize.com/tags/terminal/
6. https://pubs.opengroup.org/onlinepubs/9699919799/utilities/V3_chap02.html
7. https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html
8. https://learnxinyminutes.com/
9. https://bash.cyberciti.biz/guide/Main_Page
10. https://unix.stackexchange.com/questions/159513/what-are-the-shells-control-and-redirection-operators
11. http://linux-training.be/
