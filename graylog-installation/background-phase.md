---
description: Complete Setup guide for back end systems :D
---

# Background Phase

[GrayLog Documentation](https://go2docs.graylog.org/5-0/downloading\_and\_installing\_graylog/ubuntu\_installation.html)&#x20;

## Disabling the Firewall

For a smooth installation, it is mentioned as a pre-requisite to disable the firewall. The steps are as follows:

```bash
sudo ufw disable
```

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

## Server Timezone

Setting up a specific timezone helps to align the system with graylog

```bash
sudo timedatectl set-timezone UTC
```

## Note the Ubuntu Config System

This will be useful later on while selecting specific configurations

```bash
cat /etc/lsb-release
```

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

## Update the system

```bash
sudo apt-get update
```

