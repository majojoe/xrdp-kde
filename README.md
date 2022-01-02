**Table of Contents**

# Why xrdp-kde?
The xrdp-kde package comes with some adaptions for kde in order to work smoothly.
# Installation
Download [here](https://github.com/majojoe/xrdp-kde/releases/download/v1.0.4/xrdp-kde-1.0.4-linux-amd64.deb) and install the \*.deb package provided using the following command:
```bash
sudo apt install ./xrdp-kde-1.0.4-linux-amd64.deb
```
# Hints
In order for the TLS certificates to work out of the box the hostname including the domain should be inserted into the /etc/hosts file e.g.
```bash
127.0.1.1       hostname.domain.name hostname
# hostname, domain and name must be replaced by your actual names
```

In order to work properly with AD users the package domain_join should be installed as well:
[https://github.com/majojoe/domain_join/releases](https://github.com/majojoe/domain_join/releases)

This xrdp configuration uses TLS encryption. In order for xrdp to use a different as the local snakeoil certificates the user should provide these and point to them by changing /etc/xrdp/xrdp.ini or the adjust the links at /etc/xrdp.

