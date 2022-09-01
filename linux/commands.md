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
|[apt](https://ss64.com/bash/apt.html)|Package manager in Debian||
|[apt-get](https://ss64.com/bash/apt-get.html)|Install, upgrade and clean packages||
|[awk](https://linuxhandbook.com/awk-command-tutorial/)|Pattern scanning and text processing||
|[bg](https://ss64.com/bash/bg.html)|Run jobs in the background||
|[cat](https://ss64.com/bash/cat.html)|Join several input files by sequentially sending their content to stdout||
|[chmod](https://ss64.com/bash/chmod.html)|Change mode of access||
|[chown](https://ss64.com/bash/chown.html)|Changes ownership of files and directories||
|[crontab](https://linuxhandbook.com/crontab/)|Maintain crontab files for individual users||
|[curl](https://linuxhandbook.com/curl-command-examples/)|Transfer data. Consider using [httpie](https://github.com/httpie/httpie) instead.||
|[df](https://linuxhandbook.com/df-command/)|Report file system disk space usage||
|[diff](https://linuxhandbook.com/diff-command/)|Analyze two files and print the lines that are different||
|[dpkg](https://man7.org/linux/man-pages/man1/dpkg-query.1.html)|Package manager in Debian||
||List packages|`-l, --list [PACKAGE-NAME-PATTERN...]`|
||Report status of packages|`-s, --status [PACKAGE...]`|
||Search for packages that own files corresponding to PATTERN|`-S, --search [FILENAME-PATTERN...]`|
|[du](https://linuxhandbook.com/find-directory-size-du-command/)|Estimate file space usage||
|expand|Convert tabs to spaces||
|[export](https://linuxhandbook.com/export-command/)|Create environment variable||
|[fg](https://www.cyberciti.biz/faq/unix-linux-fg-command-examples-usage-syntax/)|Bring a background process to the foreground||
|[file](https://www.computerhope.com/unix/ufile.htm)|Determine file type|`file [OPTIONS] FILE [FILE...]`|
||brief mode|`-b, --brief`|
||output mime type strings|`-i, --mime`|
||look inside compressed file|`-z, --uncompress`|
|[free](https://www.howtogeek.com/456943/how-to-use-the-free-command-on-linux/)|Display amount of free and used memory in the system||
|[gpg](https://guides.library.illinois.edu/data_encryption/gpgcheatsheet)|Encryption and signing tool||
|hostnamectl|Control system hostname||
|[htop](https://linuxtogether.org/htop-command-explanation/)|Process viewer||
|[id](https://www.cyberciti.biz/faq/unix-linux-id-command-examples-usage-syntax/)|Print real and effective IDs of users and groups||
|[img2pdf](https://pypi.org/project/img2pdf/)|Convert raster images to PDF||
|[ip](https://www.cyberciti.biz/faq/linux-ip-command-examples-usage-syntax/)|Configure IP addresses, network interfaces, and routing rules||
|[jobs](https://www.cyberciti.biz/faq/unix-linux-jobs-command-examples-usage-syntax/)|Show active jobs in shell||
|[less](https://www.howtogeek.com/444233/how-to-use-the-less-command-on-linux/)|View contents of a text file one screen at a time||
|[ln](https://www.computerhope.com/unix/uln.htm)|Make links between files||
||[Hard link vs soft link](https://linuxgazette.net/105/pitcher.html)||
|[lscpu](https://www.cyberciti.biz/faq/lscpu-command-find-out-cpu-architecture-information/)|Display information about the CPU architecture||
|[lsof](https://www.howtogeek.com/426031/how-to-use-the-linux-lsof-command/)|List open files||
|[mc](https://tldp.org/LDP/LG/issue23/wkndmech_dec97/mc_article.html)|Directory browsing and file manipulation program||
|[md5sum](https://www.geeksforgeeks.org/md5sum-linux-command/)|Verify data integrity using MD5||
|[netcat](https://ss64.com/bash/nc.html)|Read from and write to network connections using TCP or UDP||
||Scan port range for listening deamons without sending any data|`nc -z -v HOST START_PORT-STOP_PORT`|
|netstat|Use ss instead||
|[nslookup](https://linuxhandbook.com/nslookup-command/)|Query DNS records||
|[ntpd](https://www.systutorials.com/docs/linux/man/8-ntpd/)|Network Time Protocol (NTP) daemon||
||[Sync Linux server time with Network Time servers](https://www.howtogeek.com/tips/how-to-sync-your-linux-server-time-with-network-time-servers-ntp/)||
|[ntpdate](https://www.tecmint.com/synchronize-time-with-ntp-in-linux/)|Set the date and time via NTP||
|pidof|Find the process ID of a running program||
|[pinky](https://www.howtogeek.com/427004/how-to-use-the-pinky-command-on-linux/)|Print information on system users||
|[ping](https://linuxhandbook.com/ping-command/)|Send echo request to network server||
|[printenv](https://www.cyberciti.biz/faq/linux-list-all-environment-variables-env-command/)|List environment variables||
|[ps](https://linuxhandbook.com/ps-command/)|Display information about running processes||
|[qpdf](https://qpdf.readthedocs.io/en/latest/cli.html)|Transform PDF files||
||Merge PDF files|`qpdf --empty --pages *.pdf -- out.pdf`|
||Encrypt PDF file|`qpdf --encrypt user_pass owner_pass 256 -- in.pdf encrypted_out.pdf`|
|rlwrap|Intercept user input in order to provide readline's line editing, persistent history and completion||
|[scp](https://www.linuxtechi.com/scp-command-examples-in-linux/)|Copy files over a secure, encrypted network connection||
|[set](https://www.gnu.org/software/bash/manual/html_node/The-Set-Builtin.html)|Set or unset values of shell options and positional parameters||
|[shred](https://www.computerhope.com/unix/shred.htm)|Overwrite a file to hide its contents||
|[sort](https://linuxhandbook.com/sort-command/)|Sort lines of text files||
|[source](https://ss64.com/bash/source.html)|Execute content of file in current shell||
|[ss](https://www.cyberciti.biz/tips/linux-investigate-sockets-network-connections.html)|Investigate sockets||
|[ssh](https://www.ssh.com/ssh/command/)|SSH client||
||[Local port forwarding](https://www.ssh.com/academy/ssh/tunneling/example#local-forwarding)|`ssh -L localhost:LOCAL_PORT:TARGET_HOST:TARGET_PORT JUMP_SERVER`|
|[ssh-copy-id](https://www.ssh.com/ssh/copy-id)|Install SSH key on server as authorized key||
|[ssh-keygen](https://www.ssh.com/ssh/keygen/)|Create new authentication key pairs for SSH||
|[stat](https://www.howtogeek.com/451022/how-to-use-the-stat-command-on-linux/)|Display detailed status of file or file system||
|[systemctl](https://tecadmin.net/tutorial/linux/linux-systemctl-command/)|Control systemd||
|[tar](https://linuxhandbook.com/basic-tar-commands/)|Archive and compress files||
|[taskset](https://www.howtoforge.com/linux-taskset-command/)|Set or retrieve CPU affinity||
|[tee](https://www.geeksforgeeks.org/tee-command-linux-example/)|Read from stdin and write to both stdout and one or more files||
|[tmux](https://tmuxcheatsheet.com/)|Terminal multiplexer||
|top|use htop instead||
|[tr](https://www.geeksforgeeks.org/tr-command-in-unix-linux-with-examples/)|Translate or delete characters|`tr [OPTION] SET1 [SET2]`|
||Remove new lines and save to new file|`tr -d '\n' < in.txt > out.txt`|
|[tree](https://www.geeksforgeeks.org/tree-command-unixlinux/)|List contents of directories in a tree-like format||
|[ufw](https://www.cyberciti.biz/faq/how-to-setup-a-ufw-firewall-on-ubuntu-18-04-lts-server/)|Manage netfilter firewall||
|uname|Print system information||
|[usermod](https://www.tecmint.com/usermod-command-examples/)|Modify user account||
|[visudo](https://www.computerhope.com/unix/visudo.htm)|Edit sudoers file||
|[wc](https://www.tecmint.com/wc-command-examples/)|Newline, word, byte and characters counts in files||
|[wget](https://www.computerhope.com/unix/wget.htm)|Download files over network||
|[whatis](https://www.computerhope.com/unix/whatis.htm)|Display one-line manual page descriptions||
|whereis|Locate the binary, source, and manual page files for a command||
|which|Locate the executable file associated with the given command||
|[xargs](https://www.howtogeek.com/435164/how-to-use-the-xargs-command-on-linux/)|Make commands accept standard input as arguments||
|[xxd](https://opensource.com/article/19/8/dig-binary-files-hexdump)|Make hex dump of file or stdin displaying ASCII equivalent of each byte||
|zless|View contents of compressed text file with less||

## Useful links
1. [Index of Linux commands by SS64](https://ss64.com/bash/)
1. [Explain Shell](https://explainshell.com/) - quickly lookup syntax and details of shell commands
1. [Collection of articles on Linux by Dave McKay](https://www.howtogeek.com/author/davidmckay/)
1. [Essential Linux commands by Linux Handbook](https://linuxhandbook.com/linux-commands/)
1. [Linux utilities - index (The Open Group)](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/)