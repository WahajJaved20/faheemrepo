---
description: A Recommended Step for MongoDB Setup
---

# Disabling Transparent Huge Pages (THP)

Incase if we need to add proxies in the future we can use this command

```bash
wget -qO- 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xf5679a222c647c87527c2f8cb00a0bd1e2c63c11' | sudo apt-key add -
```



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

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

4\) Configure the OS to run it on boot

```bash
sudo systemctl enable disable-transparent-huge-pages
```

