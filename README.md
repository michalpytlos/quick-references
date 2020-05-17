# Linux - quick reference

Linux commands, operators and shortcuts with descriptions. The list is not meant to be exhaustive but rather serve as a quick reference for the author.

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
|file|Determine file type|https://www.computerhope.com/unix/ufile.htm|-|
|find|Search for files|https://www.geeksforgeeks.org/find-command-in-linux-with-examples/|-|
|free|Display amount of free and used memory in the system|https://www.howtogeek.com/456943/how-to-use-the-free-command-on-linux/|-|
|gpg|Encryption and signing tool|https://www.techrepublic.com/blog/five-apps/protect-your-data-with-these-five-linux-encryption-tools/, https://guides.library.illinois.edu/data_encryption/gpgcheatsheet|-|
|grep|Print lines matching a pattern|https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/|-|
|hostnamectl|Control system hostname|man page|-|
|htop|Process viewer|https://linuxtogether.org/htop-command-explanation/|-|
|id|Print real and effective IDs of users and groups|https://www.cyberciti.biz/faq/unix-linux-id-command-examples-usage-syntax/|-|
|ip|Configure IP addresses, network interfaces, and routing rules|https://www.cyberciti.biz/faq/linux-ip-command-examples-usage-syntax/|-|
|ipython|Python shell|https://ipython.readthedocs.io/en/stable/interactive/tutorial.html|-|
|jobs|Show active jobs in shell|https://www.cyberciti.biz/faq/unix-linux-jobs-command-examples-usage-syntax/|-|
|less|View contents of a text file one screen at a time|https://www.howtogeek.com/444233/how-to-use-the-less-command-on-linux/|-|
|ln|Make links between files|https://www.computerhope.com/unix/uln.htm, https://linuxgazette.net/105/pitcher.html|-|
|lscpu|Display information about the CPU architecture|https://www.cyberciti.biz/faq/lscpu-command-find-out-cpu-architecture-information/|-|
|lsof|List open files|https://linuxhandbook.com/lsof-command/, https://www.howtogeek.com/426031/how-to-use-the-linux-lsof-command/|-|
|mc|Directory browsing and file manipulation program|https://tldp.org/LDP/LG/issue23/wkndmech_dec97/mc_article.html|-|
|md5sum|Verify data integrity using MD5|https://www.geeksforgeeks.org/md5sum-linux-command/|-|
|netstat|Use ss instead|-|-|
|nslookup|Query DNS records|https://linuxhandbook.com/nslookup-command/|-|
|ntpd|Network Time Protocol (NTP) daemon|https://www.howtogeek.com/tips/how-to-sync-your-linux-server-time-with-network-time-servers-ntp/, https://www.systutorials.com/docs/linux/man/8-ntpd/|-|
|ntpdate|Set the date and time via NTP|https://www.tecmint.com/synchronize-time-with-ntp-in-linux/|-|
|pidof|Find the process ID of a running program|man page|-|
|pinky|Print information on system users|https://www.howtogeek.com/427004/how-to-use-the-pinky-command-on-linux/||
|ping|Send echo request to network server|https://linuxhandbook.com/ping-command/|-|
|pdfunite|Merge pdfs|man page|-|
|printenv|List environment variables|https://www.cyberciti.biz/faq/linux-list-all-environment-variables-env-command/|-|
|ps|Display information about running processes|https://linuxhandbook.com/ps-command/|-|
|rlwrap|Intercept user input in order to provide readline's line editing, persistent history and completion|man page|-|
|scp|Copy files over a secure, encrypted network connection|https://www.linuxtechi.com/scp-command-examples-in-linux/|-|
|set|Set or unset values of shell options and positional parameters|https://bash.cyberciti.biz/guide/Set_command|-|
|shred|Overwrite a file to hide its contents|https://www.computerhope.com/unix/shred.htm|-|
|sort|Sort lines of text files|https://linuxhandbook.com/sort-command/|-|
|source|Execute content of file in current shell|https://ss64.com/bash/source.html|-|
|ss|Investigate sockets|https://www.cyberciti.biz/tips/linux-investigate-sockets-network-connections.html|-|
|ssh|SSH client|https://www.ssh.com/ssh/command/|-|
|ssh-copy-id|Install SSH key on server as authorized key|https://www.ssh.com/ssh/copy-id|-|
|ssh-keygen|Create new authentication key pairs for SSH|https://www.ssh.com/ssh/keygen/|-|
|stat|Display detailed status of file or file system|https://www.howtogeek.com/451022/how-to-use-the-stat-command-on-linux/|-|
|systemctl|Control systemd|https://tecadmin.net/tutorial/linux/linux-systemctl-command/|-|
|tar|Archive and compress files|https://linuxhandbook.com/basic-tar-commands/|-|
|taskset|Set or retrieve CPU affinity|https://www.howtoforge.com/linux-taskset-command/|-|
|tee|Read from stdin and write to both stdout and one or more files|https://www.geeksforgeeks.org/tee-command-linux-example/|-|
|tmux|Terminal multiplexer|https://tmuxcheatsheet.com/|-|
|top|use htop instead|-|-|
|tree|List contents of directories in a tree-like format|https://www.geeksforgeeks.org/tree-command-unixlinux/|-|
|ufw|Manage netfilter firewall|https://www.cyberciti.biz/faq/how-to-setup-a-ufw-firewall-on-ubuntu-18-04-lts-server/|-|
|uname|Print system information|man page|-|
|usermod|Modify user account|https://www.tecmint.com/usermod-command-examples/|-|
|vim|Text editor|https://linuxhandbook.com/basic-vim-commands/, https://linuxhandbook.com/vim-cheat-sheet/|-|
|visudo|Edit sudoers file|https://www.computerhope.com/unix/visudo.htm|-|
|wc|Newline, word, byte and characters counts in files|https://www.tecmint.com/wc-command-examples/|-|
|wget|Download files over network|https://www.computerhope.com/unix/wget.htm|-|
|whatis|Display one-line manual page descriptions|https://www.computerhope.com/unix/whatis.htm|-|
|whereis|Locate the binary, source, and manual page files for a command|man page|-|
|which|Locate the executable file associated with the given command|man page|-|
|xargs|Make commands accept standard input as arguments|https://www.howtogeek.com/435164/how-to-use-the-xargs-command-on-linux/|-|
|xxd|Make hex dump of file or stdin displaying ASCII equivalent of each byte|https://www.howtoforge.com/linux-xxd-command/, https://opensource.com/article/19/8/dig-binary-files-hexdump|-|
|zless|View contents of compressed text file with less|man page|-|
|zsh|Z shell|https://opensource.com/article/19/9/getting-started-zsh, https://opensource.com/article/18/9/tips-productivity-zsh|-|


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
|<<|here document| https://bash.cyberciti.biz/guide/Here_documents|

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


## Bibliography

1. https://explainshell.com/
2. https://www.howtogeek.com/author/davidmckay/
3. https://bash.cyberciti.biz/guide/Main_Page
4. http://linux-training.be/
5. https://unix.stackexchange.com/
6. https://learnxinyminutes.com/
7. https://www.tecmint.com/linux-commands-cheat-sheet/
8. https://www.howtoforge.com/linux-commands/
9. https://linuxhandbook.com/linux-commands/
10. https://linuxize.com/tags/terminal/
11. https://pubs.opengroup.org/onlinepubs/9699919799/utilities/
12. https://en.wikibooks.org/wiki/Linux_Guide
13. https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html
