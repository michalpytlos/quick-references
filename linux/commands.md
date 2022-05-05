# Linux commands - quick reference

## Contents

1. [Searching](#searching)
1. [Other commands A-Z](#Other-commands)
1. [Useful links](#useful-links)

## Searching
| command | description | usage |
| ------- |------------ | ----- |
|[grep](https://ss64.com/bash/grep.html)|Print lines matching a pattern|`grep [OPTIONS] 'PATTERN' [FILE...]`|
||print only count of selected lines per file| `-c, --count` |
||| `-i, --ignore-case` |
||print only names of files with selected lines| `-l, --files-with-matches` |
||stop after NUM selected lines|`-m NUM`|
||| `-n, --line-number` |
||show only parts of lines that match| `-o, --only-matching` |
||| `-r, --recursive` |
||match only whole words| `-w, --word-regexp` |
||select non-matching lines| `-v, --invert-match` |
||print NUM lines of trailing context| `-A NUM` |
||print NUM lines of leading context| `-B NUM` |
||print NUM lines of output context| `-C NUM` |
||PATTERNS are extended regexp| `-E, --extended-regexp` |
|[find](https://ss64.com/bash/find.html)|Search for files|`find [-H] [-L] [-P] [PATH...] [EXPRESSION]`|
||Search by filename using glob pattern|`find PATH -name 'PATTERN'`|

Useful links:
* [Introduction to grep with examples](https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/)
* [Regular expressions in grep](https://linuxize.com/post/regular-expressions-in-grep/)

## Other commands

| command | description | usage |
| ------- |------------ | --------- |
|apt-cache|Find new packages|https://itsfoss.com/apt-get-linux-guide/|
|apt-get|Install, upgrade and clean packages|https://itsfoss.com/apt-get-linux-guide/|
|awk|Pattern scanning and text processing|https://linuxhandbook.com/awk-command-tutorial/|
|bg|Run jobs in the background|https://www.cyberciti.biz/faq/unix-linux-bg-command-examples-usage-syntax/|
|cat|Join several input files by sequentially sending their content to stdout|https://linuxhandbook.com/cat-command/|
|chmod|Change mode of access|https://linuxhandbook.com/chmod-command/|
|chown|Changes ownership of files and directories|https://www.computerhope.com/unix/uchown.htm|
|crontab|Maintain crontab files for individual users|https://linuxhandbook.com/crontab/|
|curl|Transfer data|https://linuxhandbook.com/curl-command-examples/|
|df|Report file system disk space usage|https://linuxhandbook.com/df-command/|
|diff|Analyze two files and print the lines that are different|https://www.computerhope.com/unix/udiff.htm|
|dpkg|Debian package manager|https://www.cyberciti.biz/ref/apt-dpkg-ref.html|
|du|Estimate file space usage|https://linuxhandbook.com/find-directory-size-du-command/|
|expand|Convert tabs to spaces|man page|
|export|Create environment variable|https://linuxhandbook.com/export-command/|
|fg|Bring a background process to the foreground|https://www.cyberciti.biz/faq/unix-linux-fg-command-examples-usage-syntax/|
|file|Determine file type|https://www.computerhope.com/unix/ufile.htm|
|free|Display amount of free and used memory in the system|https://www.howtogeek.com/456943/how-to-use-the-free-command-on-linux/|
|gpg|Encryption and signing tool|https://www.techrepublic.com/blog/five-apps/protect-your-data-with-these-five-linux-encryption-tools/, https://guides.library.illinois.edu/data_encryption/gpgcheatsheet|
|hostnamectl|Control system hostname|man page|
|htop|Process viewer|https://linuxtogether.org/htop-command-explanation/|
|id|Print real and effective IDs of users and groups|https://www.cyberciti.biz/faq/unix-linux-id-command-examples-usage-syntax/|
|img2pdf|Convert raster images to PDF|https://pypi.org/project/img2pdf/|
|ip|Configure IP addresses, network interfaces, and routing rules|https://www.cyberciti.biz/faq/linux-ip-command-examples-usage-syntax/|
|jobs|Show active jobs in shell|https://www.cyberciti.biz/faq/unix-linux-jobs-command-examples-usage-syntax/|
|less|View contents of a text file one screen at a time|https://www.howtogeek.com/444233/how-to-use-the-less-command-on-linux/|
|ln|Make links between files|https://www.computerhope.com/unix/uln.htm, https://linuxgazette.net/105/pitcher.html|
|lscpu|Display information about the CPU architecture|https://www.cyberciti.biz/faq/lscpu-command-find-out-cpu-architecture-information/|
|lsof|List open files|https://linuxhandbook.com/lsof-command/, https://www.howtogeek.com/426031/how-to-use-the-linux-lsof-command/|
|mc|Directory browsing and file manipulation program|https://tldp.org/LDP/LG/issue23/wkndmech_dec97/mc_article.html|
|md5sum|Verify data integrity using MD5|https://www.geeksforgeeks.org/md5sum-linux-command/|
|netstat|Use ss instead|-|
|nslookup|Query DNS records|https://linuxhandbook.com/nslookup-command/|
|ntpd|Network Time Protocol (NTP) daemon|https://www.howtogeek.com/tips/how-to-sync-your-linux-server-time-with-network-time-servers-ntp/, https://www.systutorials.com/docs/linux/man/8-ntpd/|
|ntpdate|Set the date and time via NTP|https://www.tecmint.com/synchronize-time-with-ntp-in-linux/|
|pidof|Find the process ID of a running program|man page|
|pinky|Print information on system users|https://www.howtogeek.com/427004/how-to-use-the-pinky-command-on-linux/|
|ping|Send echo request to network server|https://linuxhandbook.com/ping-command/|
|printenv|List environment variables|https://www.cyberciti.biz/faq/linux-list-all-environment-variables-env-command/|
|ps|Display information about running processes|https://linuxhandbook.com/ps-command/|
|qpdf|Transform PDF files|https://qpdf.readthedocs.io/en/latest/cli.html|
||`qpdf --empty --pages *.pdf -- out.pdf`|Merge PDF files|
||`qpdf --encrypt user_pass owner_pass 256 -- in.pdf encrypted_out.pdf`|Encrypt PDF file|
|rlwrap|Intercept user input in order to provide readline's line editing, persistent history and completion|man page|
|scp|Copy files over a secure, encrypted network connection|https://www.linuxtechi.com/scp-command-examples-in-linux/|
|set|Set or unset values of shell options and positional parameters|https://bash.cyberciti.biz/guide/Set_command|
|shred|Overwrite a file to hide its contents|https://www.computerhope.com/unix/shred.htm|
|sort|Sort lines of text files|https://linuxhandbook.com/sort-command/|
|source|Execute content of file in current shell|https://ss64.com/bash/source.html|
|ss|Investigate sockets|https://www.cyberciti.biz/tips/linux-investigate-sockets-network-connections.html|
|ssh|SSH client|https://www.ssh.com/ssh/command/|
||`ssh -L localhost:LOCAL_PORT:TARGET_HOST:TARGET_PORT JUMP_SERVER`|[Local port forwarding](https://www.ssh.com/academy/ssh/tunneling/example#local-forwarding)|
|ssh-copy-id|Install SSH key on server as authorized key|https://www.ssh.com/ssh/copy-id|
|ssh-keygen|Create new authentication key pairs for SSH|https://www.ssh.com/ssh/keygen/|
|stat|Display detailed status of file or file system|https://www.howtogeek.com/451022/how-to-use-the-stat-command-on-linux/|
|systemctl|Control systemd|https://tecadmin.net/tutorial/linux/linux-systemctl-command/|
|tar|Archive and compress files|https://linuxhandbook.com/basic-tar-commands/|
|taskset|Set or retrieve CPU affinity|https://www.howtoforge.com/linux-taskset-command/|
|tee|Read from stdin and write to both stdout and one or more files|https://www.geeksforgeeks.org/tee-command-linux-example/|
|tmux|Terminal multiplexer|https://tmuxcheatsheet.com/|
|top|use htop instead|-|
|tree|List contents of directories in a tree-like format|https://www.geeksforgeeks.org/tree-command-unixlinux/|
|ufw|Manage netfilter firewall|https://www.cyberciti.biz/faq/how-to-setup-a-ufw-firewall-on-ubuntu-18-04-lts-server/|
|uname|Print system information|man page|
|usermod|Modify user account|https://www.tecmint.com/usermod-command-examples/|
|vim|Text editor|https://linuxhandbook.com/basic-vim-commands/, https://linuxhandbook.com/vim-cheat-sheet/|
|visudo|Edit sudoers file|https://www.computerhope.com/unix/visudo.htm|
|wc|Newline, word, byte and characters counts in files|https://www.tecmint.com/wc-command-examples/|
|wget|Download files over network|https://www.computerhope.com/unix/wget.htm|
|whatis|Display one-line manual page descriptions|https://www.computerhope.com/unix/whatis.htm|
|whereis|Locate the binary, source, and manual page files for a command|man page|
|which|Locate the executable file associated with the given command|man page|
|xargs|Make commands accept standard input as arguments|https://www.howtogeek.com/435164/how-to-use-the-xargs-command-on-linux/|
|xxd|Make hex dump of file or stdin displaying ASCII equivalent of each byte|https://www.howtoforge.com/linux-xxd-command/, https://opensource.com/article/19/8/dig-binary-files-hexdump|
|zless|View contents of compressed text file with less|man page|

## Useful links
1. [Index of Linux commands by SS64](https://ss64.com/bash/)
1. [Explain Shell](https://explainshell.com/) - quickly lookup syntax and details of shell commands
1. [Collection of articles on Linux by Dave McKay](https://www.howtogeek.com/author/davidmckay/)
1. [Essential Linux commands by Linux Handbook](https://linuxhandbook.com/linux-commands/)
1. [Linux utilities - index (The Open Group)](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/)