# Linux commands - quick reference

## Contents

1. [Searching](#searching)
1. [Text viewing and manipulation](#text-viewing-and-manipulation)
1. [Processes](#processes)
1. [Remote machines](#remote-machines)
1. [Network utils](#network-utils)
1. [Scripting](#scripting)
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
|[ripgrep](https://github.com/BurntSushi/ripgrep#readme)|Modern alternative to grep|`rg [OPTIONS] 'PATTERN' [PATH...]`|
||Only search files matching TYPE|`-t, --type TYPE`|
||List all available types|`--type-list`|
||Print files that would be searched|`--files`|
|[find](https://ss64.com/bash/find.html)|Search for files|`find [-H] [-L] [-P] [PATH...] [EXPRESSION]`|
||Search by filename using glob pattern|`find PATH -name 'PATTERN'`|
|[fzf](https://github.com/junegunn/fzf#table-of-contents)|Fuzzy finder||
||Select file and open in Neovim|`nvim $(fzf)`|

Useful links:
* [Introduction to grep with examples](https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/)
* [Regular expressions in grep](https://linuxize.com/post/regular-expressions-in-grep/)

## Text viewing and manipulation
| command | description | usage |
| ------- |------------ | --------- |
|[awk](https://linuxhandbook.com/awk-command-tutorial/)|Pattern scanning and text processing||
|[cat](https://ss64.com/bash/cat.html)|Join several input files by sequentially sending their content to stdout||
||display nonprinting chars except for line feed (LFD) and TAB|`-v, --show-nonprinting`|
||display `$` at end of each line|`-E, --show-ends`|
||display TAB chars as `^I`|`-T, --show-tabs`|
||equivalent to `-vET`|`-A, --show-all`|
|[diff](https://linuxhandbook.com/diff-command/)|Analyze two files and print the lines that are different||
|expand|Convert tabs to spaces||
|head|print first 10 lines of each FILE to stdout|`head [OPTIONS] [FILE...]`|
|[less](https://www.howtogeek.com/444233/how-to-use-the-less-command-on-linux/)|View contents of a text file one screen at a time||
|[rich-cli](https://github.com/Textualize/rich-cli)|syntax highlight text from file or command line||
|sed|stream editor||
||print lines `5` to `10` of file|`sed -n '5,10p' FILE`|
||substitute `old` with `new`|`sed -i 's/old/new/g' FILE`|
||delete all lines containing pattern|`sed -i '/PATTERN/d' FILE`|
||delete lines from `5` to the end of file|`sed -i '5,$d' FILE`|
|[sort](https://linuxhandbook.com/sort-command/)|Sort lines of text files||
|tail|print last 10 lines of each FILE to stdout|`tail [OPTIONS] [FILE...]`|
||output appended data as the file grows|`-f, --follow`|
||print last `NUM` lines|`-n NUM`|
||print lines starting with line `NUM`|`-n +NUM`|
|[tr](https://www.geeksforgeeks.org/tr-command-in-unix-linux-with-examples/)|Translate or delete characters|`tr [OPTION] SET1 [SET2]`|
||Remove new lines and save to new file|`tr -d '\n' < in.txt > out.txt`|
|[wc](https://www.tecmint.com/wc-command-examples/)|Newline, word, byte and characters counts in files||
|zless|View contents of compressed text file with less||

## Processes
| command | description | usage |
| ------- |------------ | --------- |
|[htop](https://linuxtogether.org/htop-command-explanation/)|Process viewer||
|lsof|List open files||
||limit to process|`-p PID`|
||limit to user|`-u USER`|
||limit to directory|`+D DIRECTORY`|
||display information about network connections|`-i`|
||display port numbers (not port names)|`-P`|
||display IP addresses (not hostnames)|`-n`|
||specify socket type and state filter|`-s SOCKET_TYPE:STATE`|
||list listening TCP ports |`sudo lsof -i -P -n -s TCP:LISTEN`|
|pgrep|List PIDs of processes matching pattern|`pgrep [OPTIONS] PATTERN`|
||Show only processes owned by user|`-u USER`|
|pidof|Find the process ID of a running program||
|pkill|Send specified signal to processes|`pkill [OPTIONS] PATTERN`|
||Send SIGKILL|`-9`|
|ps|Display information about running processes||
||Show all processes|`-e`|
||Extra full format|`-F`|
||Show processes owned by user|`-u USER`|
|pstree|Display tree of processes|`pstree [OPTIONS] [PID, USER]`|
||Show PIDs|`-p`|
||Show UID (User Identifier) transitions|`-u`|

## Remote machines
| command | description | usage |
| ------- |------------ | --------- |
|scp|Copy files over a secure, encrypted network connection|`scp [OPTIONS] SOURCE TARGET`|
||Copy to remote server|`scp /path/to/local/file user@remote_server:/destination/path`|
||Recursive copy|`-r`|
|[ssh](https://www.ssh.com/ssh/command/)|SSH client||
||Execute command on remote server|`ssh remote_server 'command'`|
||[SSH tunneling](https://www.ssh.com/academy/ssh/tunneling/example#local-forwarding). Forward local port to port on target server through jump server|`ssh -L localhost:LOCAL_PORT:TARGET_HOST:TARGET_PORT JUMP_SERVER`|
||Forward local port to port on remote server|`ssh -L localhost:LOCAL_PORT:localhost:REMOTE_PORT USER@REMOTE_SERVER`|
|[ssh-copy-id](https://www.ssh.com/ssh/copy-id)|Install SSH key on server as authorized key||
|[ssh-keygen](https://www.ssh.com/ssh/keygen/)|Create new authentication key pairs for SSH||

## Network utils
| command | description | usage |
| ------- |------------ | --------- |
|curl|Transfer data to or from server|`curl [OPTIONS] URL`|
||Specify HTTP request method|`-X METHOD`|
||Extra header in HTTP request|`-H 'HEADER_NAME: HEADER_VALUE'`|
||Send data in POST request to HTTP server|`-d 'DATA'`|
||Send JSON payload to HTTP server|`curl -X POST -H 'Content-Type: application/json' -d '{"key1":"val1","key2":"val2"}' URL`|
||Specify file to which write all cookies after completed operation|`-c, --cookie-jar FILE`|
||Pass data to server in cookie header|`-b, --cookie (DATA \| FILE)`|
||Include HTTP response headers in output|`-i, --include`|
||Write output to file instead of stdout|`-o, --output FILE`|
|[httpie](https://github.com/httpie/httpie)|Command-line http client||
|[netcat](https://ss64.com/bash/nc.html)|Read from and write to network connections using TCP or UDP||
||Scan port range for listening deamons without sending any data|`nc -zv HOST START_PORT-STOP_PORT`|
|netstat|Use ss instead||
|[nslookup](https://linuxhandbook.com/nslookup-command/)|Query DNS records||
|[ping](https://linuxhandbook.com/ping-command/)|Send echo request to network server||
|[ss](https://www.cyberciti.biz/tips/linux-investigate-sockets-network-connections.html)|Investigate sockets||
|[wget](https://www.computerhope.com/unix/wget.htm)|Download files over network||

## Scripting
| command | description | usage |
| ------- |------------ | --------- |
|[getopts](https://www.howtogeek.com/778410/how-to-use-getopts-to-parse-linux-shell-script-options/)|Process command line args||
|trap|Set up signal handling by script or shell|`trap COMMAND SIGNAL [SIGNAL...]`|

## Other commands
| command | description | usage |
| ------- |------------ | --------- |
|[apt](https://ss64.com/bash/apt.html)|Package manager in Debian||
|[apt-get](https://ss64.com/bash/apt-get.html)|Install, upgrade and clean packages||
|[bg](https://ss64.com/bash/bg.html)|Run jobs in the background||
|[chmod](https://ss64.com/bash/chmod.html)|Change mode of access||
|[chown](https://ss64.com/bash/chown.html)|Changes ownership of files and directories||
|[crontab](https://linuxhandbook.com/crontab/)|Maintain crontab files for individual users||
|[df](https://linuxhandbook.com/df-command/)|Report file system disk space usage||
|[dpkg](https://man7.org/linux/man-pages/man1/dpkg-query.1.html)|Package manager in Debian||
||List packages|`-l, --list [PACKAGE-NAME-PATTERN...]`|
||Report status of packages|`-s, --status [PACKAGE...]`|
||Search for packages that own files corresponding to PATTERN|`-S, --search [FILENAME-PATTERN...]`|
|[du](https://linuxhandbook.com/find-directory-size-du-command/)|Estimate file space usage||
|[export](https://linuxhandbook.com/export-command/)|Create environment variable||
|[fg](https://www.cyberciti.biz/faq/unix-linux-fg-command-examples-usage-syntax/)|Bring a background process to the foreground||
|[file](https://www.computerhope.com/unix/ufile.htm)|Determine file type|`file [OPTIONS] FILE [FILE...]`|
||brief mode|`-b, --brief`|
||output mime type strings|`-i, --mime`|
||look inside compressed file|`-z, --uncompress`|
|[free](https://www.howtogeek.com/456943/how-to-use-the-free-command-on-linux/)|Display amount of free and used memory in the system||
|[gpg](https://guides.library.illinois.edu/data_encryption/gpgcheatsheet)|Encryption and signing tool||
|hostnamectl|Control system hostname||
|[id](https://www.cyberciti.biz/faq/unix-linux-id-command-examples-usage-syntax/)|Print real and effective IDs of users and groups||
|[img2pdf](https://pypi.org/project/img2pdf/)|Convert raster images to PDF||
|[ip](https://www.cyberciti.biz/faq/linux-ip-command-examples-usage-syntax/)|Configure IP addresses, network interfaces, and routing rules||
|[jobs](https://www.cyberciti.biz/faq/unix-linux-jobs-command-examples-usage-syntax/)|Show active jobs in shell||
|[ln](https://www.computerhope.com/unix/uln.htm)|Make links between files||
||[Hard link vs soft link](https://linuxgazette.net/105/pitcher.html)||
|[lscpu](https://www.cyberciti.biz/faq/lscpu-command-find-out-cpu-architecture-information/)|Display information about the CPU architecture||
|[mc](https://tldp.org/LDP/LG/issue23/wkndmech_dec97/mc_article.html)|Directory browsing and file manipulation program||
|[md5sum](https://www.geeksforgeeks.org/md5sum-linux-command/)|Verify data integrity using MD5||
|[ntpd](https://www.systutorials.com/docs/linux/man/8-ntpd/)|Network Time Protocol (NTP) daemon||
||[Sync Linux server time with Network Time servers](https://www.howtogeek.com/tips/how-to-sync-your-linux-server-time-with-network-time-servers-ntp/)||
|[ntpdate](https://www.tecmint.com/synchronize-time-with-ntp-in-linux/)|Set the date and time via NTP||
|[pinky](https://www.howtogeek.com/427004/how-to-use-the-pinky-command-on-linux/)|Print information on system users||
|[printenv](https://www.cyberciti.biz/faq/linux-list-all-environment-variables-env-command/)|List environment variables||
|[qpdf](https://qpdf.readthedocs.io/en/latest/cli.html)|Transform PDF files||
||Merge PDF files|`qpdf --empty --pages *.pdf -- out.pdf`|
||Encrypt PDF file|`qpdf --encrypt user_pass owner_pass 256 -- in.pdf encrypted_out.pdf`|
|rlwrap|Intercept user input in order to provide readline's line editing, persistent history and completion||
|[set](https://www.gnu.org/software/bash/manual/html_node/The-Set-Builtin.html)|Set or unset values of shell options and positional parameters||
|[shred](https://www.computerhope.com/unix/shred.htm)|Overwrite a file to hide its contents||
|[source](https://ss64.com/bash/source.html)|Execute content of file in current shell||
|[stat](https://www.howtogeek.com/451022/how-to-use-the-stat-command-on-linux/)|Display detailed status of file or file system||
|[systemctl](https://tecadmin.net/tutorial/linux/linux-systemctl-command/)|Control systemd||
|[tar](https://linuxhandbook.com/basic-tar-commands/)|Archive and compress files||
|[taskset](https://www.howtoforge.com/linux-taskset-command/)|Set or retrieve CPU affinity||
|[tee](https://www.geeksforgeeks.org/tee-command-linux-example/)|Read from stdin and write to both stdout and one or more files||
|[tmux](https://tmuxcheatsheet.com/)|Terminal multiplexer||
|[tree](https://www.geeksforgeeks.org/tree-command-unixlinux/)|List contents of directories in a tree-like format||
|[ufw](https://www.cyberciti.biz/faq/how-to-setup-a-ufw-firewall-on-ubuntu-18-04-lts-server/)|Manage netfilter firewall||
|uname|Print system information||
|[usermod](https://www.tecmint.com/usermod-command-examples/)|Modify user account||
|[visudo](https://www.computerhope.com/unix/visudo.htm)|Edit sudoers file||
|[whatis](https://www.computerhope.com/unix/whatis.htm)|Display one-line manual page descriptions||
|whereis|Locate the binary, source, and manual page files for a command||
|which|Locate the executable file associated with the given command||
|[xargs](https://www.howtogeek.com/435164/how-to-use-the-xargs-command-on-linux/)|Make commands accept standard input as arguments||
|[xxd](https://opensource.com/article/19/8/dig-binary-files-hexdump)|Make hex dump of file or stdin displaying ASCII equivalent of each byte||

## Useful links
1. [Index of Linux commands by SS64](https://ss64.com/bash/)
1. [Explain Shell](https://explainshell.com/) - quickly lookup syntax and details of shell commands
1. [Linux utilities - index (The Open Group)](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/)