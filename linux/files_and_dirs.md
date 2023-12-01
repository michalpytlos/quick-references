# Important files and directories in Linux (Debian)

## Directories

To get information on the purpose of the typical default Linux directories run: `man hier`

## Important files

| file | description | usage |
| -----| ----------- | ----- |
| [/etc/apt/sources.list](https://manpages.debian.org/bookworm/apt/sources.list.5.en.html) | list of sources from which apt packages can be obtained||
|[/etc/apt/sources.list.d](https://manpages.debian.org/bookworm/apt/sources.list.5.en.html#SOURCES.LIST.D)|directory with additional source.list entries stored in separate files||
| /etc/services | file mapping services to port numbers ||
| [/etc/hosts](https://man7.org/linux/man-pages/man5/hosts.5.html)| static lookup table for hostnames ||
| [/etc/passwd](https://www.cyberciti.biz/faq/understanding-etcpasswd-file-format/) | user account info ||
| /etc/group | group account info |||
| [/etc/sudoers](https://www.sudo.ws/man/1.8.15/sudoers.man.html) | sudoers file - list of who can run what ||
| [/dev/null](https://stackoverflow.com/a/50267975)|null device file that discards all data written to it||
||redirect stdout and stderr produced by COMMAND to the null device|`COMMAND &> /dev/null `|
||send EOF to COMMAND immediately when it tries to read from stdin|`COMMAND < /dev/null`|
