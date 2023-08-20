# Miscellaneous

## Software development
1. [Martin Fowler](https://martinfowler.com/)
1. [Feature flags](https://martinfowler.com/articles/feature-toggles.html)

## Code review
1. [Conventional Comments](https://conventionalcomments.org/) - standard for formatting review comments
1. [Code Review Developer Guide by Google](https://google.github.io/eng-practices/review/)

## Web development
1. [HTTP methods](https://github.com/for-GET/know-your-http-well/blob/master/methods.md)
1. [HTTP status codes](https://github.com/for-GET/know-your-http-well/blob/master/status-codes.md)
1. [HTTP status code decision diagram](https://github.com/for-GET/http-decision-diagram)
1. [HTTP references by Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTTP)

## Kubernetes
1. [kubectx](https://github.com/ahmetb/kubectx) - switch between contexts (clusters) on kubectl faster
1. [kubens](https://github.com/ahmetb/kubectx) - switch between namespaces on kubectl faster

## WSL

### Docker setup without Docker Desktop (Win 11 + Ubuntu 22.04):
#### PowerShell
1. Check if target Linux distro is running on WSL2: `wsl -l -v`
1. If WSL1, upgrade: `wsl --set-version <distro name> 2`

#### Linux distro
1. Switch to legacy iptables:
	* `sudo update-alternatives --set iptables /usr/sbin/iptables-legacy`
	* `sudo update-alternatives --set ip6tables /usr/sbin/ip6tables-legacy`
1. Install Docker: [docs](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)
1. (Optional) Manage Docker as non-root user: `sudo usermod -aG docker $USER` [docs](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user)

#### Windows 10
* If there is no `systemd`, Docker daemon has to be run manually for Docker to work: `sudo dockerd`
* `systemd` is only available in distros running on Win 11 - see [Microsoft blog](https://devblogs.microsoft.com/commandline/systemd-support-is-now-available-in-wsl/) for more info.

