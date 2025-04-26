All Packages are in Some Repositories. OS can access them by url.
We can add some repositories to that list like VAGRANT in previous session.

**Note:** wen need GPG key for making a repository trusted. It make us sure that we directly get packages from that repository.
### APT
```shell
apt install PACKAGE_NAME
apt remove {--purge} PACKAGE_NAME
apt autoremove
apt update
apt upgrade -y
apt-key list  #Show List of GPG keys
apt list --upgradable #Check the list would be upgrade when we call apt upgrade command
```
### Install .deb files
```shell
sudo dpkg -i FILE_NAME
```

**Note:** When we see 2 file like *source.list* and *source.list.d*, second one have more data than first one. from new version of Ubuntu, \*.d convert to directory and all the repositories are included in categories by app names.

### Set Proxy for apt
```shell
nano /etc/apt/apt.conf.d/01proxy
```

```shell
Acquire::http::Proxy "http://127.0.0.1:8123";
Acquire::https::Proxy "https://127.0.1.0:8123";
```
```shell
export HTTP_PROXY=http://127.0.0.1:9898
export HTTPS_PROXY=https://127.0.0.1:9898
```
### Debian Packages Source
[Debian Packages Source](https://www.debian.org/distrib/packages)



