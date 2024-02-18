# Accessing the Graylog Web interface

Open the Graylog server configuration file

```bash
sudo nano /etc/graylog/server/server.conf
```

Press Ctrl+W to search for the keyword "http\_bind"

Uncomment the statement and assign it your VMs IP Address

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Finally, save it.

Enable and restart the service again,

