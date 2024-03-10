# Graylog Setup

## Java Installation

Run the following command to setup Java

```bash
sudo apt-get install apt-transport-https openjdk-8-jre-headless uuid-runtime pwgen
```

## MongoDB Installation

Retrieve the Key

```bash
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
```

Get MongoDB

```bash
echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list
```

Update package repositories

```bash
sudo apt-get update --allow-unauthenticated --allow-insecure-repositories
```

Install MongoDB

```bash
sudo apt-get install -y --allow-unauthenticated mongodb-org
```

Reload Daemon Processes

```bash
sudo systemctl daemon-reload
```

Enable mongodb service

```bash
sudo systemctl enable mongod.service
```

Restart mongoDB service

```bash
sudo systemctl restart mongod.service
```

Check MongoDB Status

```bash
sudo systemctl --type=service --state=active | grep mongod
```

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Elastic Search Installation

Get the Elastic Search Key

```bash
wget -q https://artifacts.elastic.co/GPG-KEY-elasticsearch -O myKey
```

Add the Key

```bash
sudo apt-key add myKey
```

Get the repository

```bash
echo "deb https://artifacts.elastic.co/packages/oss-6.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-6.x.list
```

Update the Package Lists

```bash
sudo apt-get update --allow-unauthenticated --allow-insecure-repositories
```

Install the Package

```bash
sudo apt-get install --allow-unauthenticated elasticsearch-oss
```

Modify the Elastic Search Config file

```bash
sudo tee -a /etc/elasticsearch/elasticsearch.yml > /dev/null <<EOT
> cluster.name: graylog
> action.auto_create_index: false
> EOT
```

Reload Daemon Proccesses

```bash
sudo systemctl daemon-reload
```

Enable Elastic Search Service

```bash
sudo systemctl enable elasticsearch.service
```

Restart Elastic search service

```bash
sudo systemctl restart elasticsearch.service
```

Check Elastic search status

```bash
sudo systemctl --type=service --state=active | grep elasticsearch
```

## Graylog Installation

Download the repository

```bash
wget https://packages.graylog2.org/repo/packages/graylog-3.3-repository_latest.deb
```

Unpack the package

```bash
sudo dpkg -i graylog-3.3-repository_latest.deb
```

Update the Package Lists

```bash
sudo apt-get update --allow-unauthenticated --allow-insecure-repositories
```

Install the Package

```bash
sudo apt-get install --allow-unauthenticated graylog-server
```

Reload Daemon Proceses

```bash
sudo systemctl daemon-reload
```

Configure Graylog

```bash
# Create a password secret
pwgen -N 1 -s 96
# generate a SHA256 password
echo -n 123456 | sha256sum
sudo nano /etc/graylog/server/server.conf
# Add the pwgen result in password secret and sha256 in root password
```

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Enable graylog service

```bash
sudo systemctl enable graylog-server.service
```

Restart graylog service

```bash
sudo systemctl restart graylog-server.service
```

Check graylog status

```bash
sudo systemctl --type=service --state=active | grep graylog-server
```

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
