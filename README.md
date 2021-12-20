**Table of Contents**

# Why xrdp-kde?
The xrdp-kde package comes with some adaptions for kde in order to work smoothly.
# Installation
Download [here](https://github.com/majojoe/xrdp-kde/releases/download/v1.0.0/xrdp-kde-1.0.0-linux-amd64.deb) and install the \*.deb package provided using the following command:
```bash
sudo apt install ./xrdp-kde-1.0.0-linux-amd64.deb
```
# Hints
In order for the TLS certificates to work out of the box the hostname including the domain should be inserted into the /etc/hosts file e.g.
```bash
127.0.1.1       hostname.domain.name hostname
# hostname, domain and name must be replaced by your actual names
```
