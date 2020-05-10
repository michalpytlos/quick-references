# Linux - quick reference

List of common linux commands, operators and shortcuts with descriptions. The list is not meant to be exhaustive but rather serve as a quick reference for the author.

## Table of contents
- [Commands](#commands)
- [Shell operators](#shell-operators)
  * [Control operators](#control-operators)
  * [Redirection operators](#redirection-operators)
- [Shortcuts](#shortcuts)
  * [Command line](#command-line)
  * [Desktop](#desktop)
  * [Terminal window](#terminal-window)
- [Files](#files)
- [Closer look at selected tools](#closer-look-at-selected-tools)
- [Bibliography](#bibliography)


## Commands

| command | description | more info | tags |
| ------- |------------ | --------- | ---- |
|apt-cache|Find new packages|https://itsfoss.com/apt-get-linux-guide/|-|
|apt-get|Install, upgrade and clean packages|https://itsfoss.com/apt-get-linux-guide/|-|
|awk|Pattern scanning and text processing|https://linuxhandbook.com/awk-command-tutorial/|-|
|bg|Run jobs in the background|https://www.cyberciti.biz/faq/unix-linux-bg-command-examples-usage-syntax/|-|
|cat|Join several input files by sequentially sending their content to stdout|https://linuxhandbook.com/cat-command/|-|
|chmod|Change mode of access|https://linuxhandbook.com/chmod-command/|-|
|chown|Changes ownership of files and directories|https://www.computerhope.com/unix/uchown.htm|-|
|crontab|Maintain crontab files for individual users|https://linuxhandbook.com/crontab/|-|
|curl|Transfer data|https://linuxhandbook.com/curl-command-examples/|-|
|df|Report file system disk space usage|https://linuxhandbook.com/df-command/|-|
|diff|Analyze two files and print the lines that are different|https://www.computerhope.com/unix/udiff.htm|-|
|dpkg|Debian package manager|https://www.cyberciti.biz/ref/apt-dpkg-ref.html|-|
|du|Estimate file space usage|https://linuxhandbook.com/find-directory-size-du-command/|-|
|export|Create environment variable|https://linuxhandbook.com/export-command/|-|
|fg|Bring a background process to the foreground|https://www.cyberciti.biz/faq/unix-linux-fg-command-examples-usage-syntax/|-|
|find|Search for files|https://www.geeksforgeeks.org/find-command-in-linux-with-examples/|-|
|free|Display amount of free and used memory in the system|https://www.howtogeek.com/456943/how-to-use-the-free-command-on-linux/|-|
|gpg|Encryption and signing tool|https://www.techrepublic.com/blog/five-apps/protect-your-data-with-these-five-linux-encryption-tools/, https://guides.library.illinois.edu/data_encryption/gpgcheatsheet|-|
|grep|Print lines matching a pattern|https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/|-|
|hostname|-|-|-|
|hostnamectl|-|-|-|
|id|-|-|-|
|ip|-|-|-|
|ipconfig|-|-|-|
|ipython|-|-|-|
|jobs|-|-|-|
|less|-|-|-|
|ln|-|-|-|
|lscpu|-|-|-|
|lsof|-|-|-|
|mc|-|-|-|
|md5sum|-|-|-|
|mkdir|-|-|-|
|mount|-|-|-|
|netstat|-|-|-|
|nslookup|-|-|-|
|ping|Send echo request to network server|https://linuxhandbook.com/ping-command/|-|
|pdfunite|-|-|-|
|ps|-|-|-|
|rlwrap|-|-|-|
|scp|-|-|-|
|set|-|-|-|
|shred|-|-|-|
|sort|-|-|-|
|source|Execute content of file in current shell|https://ss64.com/bash/source.html|-|
|ssh|-|-|-|
|ssh-copy-id|-|-|-|
|ssh-keygen|-|-|-|
|stat|-|-|-|
|systemctl|-|-|-|
|systemd|-|-|-|
|tar|-|-|-|
|taskset|-|-|-|
|tee|-|-|-|
|tmux|-|-|-|
|top|-|-|-|
|tree|-|-|-|
|ufw|-|-|-|
|uname|-|-|-|
|usermod|-|-|-|
|vim|-|-|-|
|visudo|-|-|-|
|wc|-|-|-|
|wget|-|-|-|
|whereis|-|-|-|
|which|-|-|-|
|xargs|-|-|-|
|xxd|-|-|-|
|zless|-|-|-|


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
|>>|Direct stdout of command into file. Append to the file.|command > out.txt|
|&>|Direct both stdout and stderr of command into file|command &> out_err.txt|
|&>>|Direct both stdout and stderr of command into file. Append to the file.|command &>> out_err.txt|
|<<|here document. See https://bash.cyberciti.biz/guide/Here_documents for more info|||

References:
1. http://linux-training.be/funhtml/ch13.html
2. https://unix.stackexchange.com/questions/159513/what-are-the-shells-control-and-redirection-operators


## Shortcuts
### Command line
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

### Desktop
| Shortcut | description |
| ---------| ----------- |
|super + d|Minimize all windows|
|super + h|Minimize/hide current window|
|super + tab|Switch applications|
|super + <arrow_key>|Control size and position of application window|
|ctrl + alt + up arrow|Move to the previous workspace|

### Terminal window
| Shortcut | description |
| ---------| ----------- |
|ctrl + alt + t|Open new terminal window|
|shift + ctrl + t|Open new tab in terminal window|
|alt + <tab_number>|Switch to tab <tab_number>|

References:
1. https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/
2. https://www.howtogeek.com/howto/41418/how-to-be-more-productive-in-ubuntu-using-keyboard-shortcuts/


## Files

To get information on the purpose of the typical default Linux directories run: `man hier`

| file | description | more info |
| -----| ----------- | --------- |
| /etc/services | file mapping services to port numbers ||
| /etc/passwd | user account info |https://www.cyberciti.biz/faq/understanding-etcpasswd-file-format/ |
| /etc/group | group account info ||
| /etc/sudoers | sudoers file - list of who can run what |https://www.sudo.ws/man/1.8.15/sudoers.man.html|


## Closer look at selected tools


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
12. https://linuxhandbook.com/linux-commands/
