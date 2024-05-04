# WSL - quick reference

## Commands

| Command | description |
| ------- | ----------- |
| `wsl --shutdown` |Terminate all running distros and WSL |
| `wsl -l -v`|Show detailed info about all distros|
| `wsl -l -o`|List distros that can be installed|
| `wsl -d <distro>`|Run distro|
| `wsl -t <distro>`|Terminate/stop distro|
| `wsl --update`| Update WSL. See [release page](https://github.com/microsoft/WSL/releases) for changelog.|

## Configuration
* [wsl.conf](https://github.com/MicrosoftDocs/wsl/blob/main/WSL/wsl-config.md#wslconf)
* [.wslconfig](https://github.com/MicrosoftDocs/wsl/blob/main/WSL/wsl-config.md#wslconfig)

## Docker setup without Docker Desktop (Win 11 + Ubuntu 22.04):
### PowerShell
1. Check if target Linux distro is running on WSL2: `wsl -l -v`
1. If WSL1, upgrade: `wsl --set-version <distro name> 2`

### Linux distro
1. Switch to legacy iptables:
	* `sudo update-alternatives --set iptables /usr/sbin/iptables-legacy`
	* `sudo update-alternatives --set ip6tables /usr/sbin/ip6tables-legacy`
1. Install Docker: [docs](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)
1. (Optional) Manage Docker as non-root user: `sudo usermod -aG docker $USER` [docs](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user)

### Windows 10
* Enable `systemd`: add to `/etc/wsl.conf`:
```
[boot]
systemd=true
```
* If there is no `systemd`, Docker daemon has to be run manually for Docker to work: `sudo dockerd`
