# Local MongoDB Setup (Will be added later)

Incase if we need to add proxies in the future we can use this command

```bash
wget -qO- 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xf5679a222c647c87527c2f8cb00a0bd1e2c63c11' | sudo apt-key add -
```

## Disable Transparent Huge Pages (THP)

Transparent Huge Pages (THP) is a Linux memory management system that reduces the overhead of Translation Lookaside Buffer (TLB) lookups on machines with large amounts of memory by using larger memory pages.

However, database workloads often perform poorly with THP enabled, because they tend to have sparse rather than contiguous memory access patterns.

1\) Create a systemd file

Add this file at the path with the command

```bash
sudo nano /etc/systemd/system/disable-transparent-huge-pages.service
```

Add the following contents to the file

```bash
[Unit]
Description=Disable Transparent Huge Pages (THP)
DefaultDependencies=no
After=sysinit.target local-fs.target
Before=mongod.service

[Service]
Type=oneshot
ExecStart=/bin/sh -c 'echo never | tee /sys/kernel/mm/transparent_hugepage/enabled > /dev/null'

[Install]
WantedBy=basic.target

```

2\) Reload the systemd files

```bash
sudo systemctl daemon-reload
```

3\) Restart the service

i) Start the service manually once to ensure that the appropriate THP setting has been changed

```bash
sudo systemctl start disable-transparent-huge-pages
```

ii) Verify that THP has successfully been set to `[never]` by running the following command

```bash
cat /sys/kernel/mm/transparent_hugepage/enabled
```

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

4\) Configure the OS to run it on boot

```bash
sudo systemctl enable disable-transparent-huge-pages
```

## Installation

### Importing the Public Key for Package Management System

1\) Installing Relevant Packages

```bash
sudo apt-get install gnupg curl
```

2\) Retrieving the Key

```bash
curl -fsSL https://www.mongodb.org/static/pgp/server-7.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
   --dearmor
```

#### Creating a List file for mongoDB

```bash
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
```

#### Reload Package Database

```bash
sudo apt-get update
```

#### Finally install the MongoDB Package

```bash
sudo apt-get install -y mongodb-org
```
