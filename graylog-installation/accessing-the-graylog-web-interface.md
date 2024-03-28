# Accessing the Graylog Web interface

Re-enable Firewall

```bash
sudo ufw enable
```

Allow connections via port 9000(for graylog) and port 22(for SSH)

```bash
sudo ufw allow 9000
sudo ufw allow 22
```

Open the Graylog server configuration file

```bash
sudo nano /etc/graylog/server/server.conf
```

Press Ctrl+W to search for the keyword "http\_bind\_address"

Uncomment the statement and assign it (0.0.0.0)

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Finally, save it.

Restart Graylog service again.

```bash
sudo systemctl restart graylog-server.service
```

Finally, check the status to see if its running.

```bash
sudo systemctl status graylog-server
```

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

At last, In your Host Machine, open a Browser in **"Incognito Mode"** and type http://\<VM\_IP>:9000

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

ANDDDD VOILA!!!!

THE WEB INTERFACE IS ACCESSIBLE TO YOUR HOST MACHINE.

The credentials should be \<admin>:\<the password whose SHA256 you generated>

After entering the credentials, WE ARE IN.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>
