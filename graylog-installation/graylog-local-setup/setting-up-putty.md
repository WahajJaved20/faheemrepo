# Setting up Putty

Since, we cant paste commands in ubuntu server, we will use a software called Putty to establish an SSH connection to the ubuntu server.

Download Link: [https://www.putty.org](https://www.putty.org)

## Make the VM visible publicly

To get an IP assigned so we can connect via SSH, go to network settings in vitual box and select bridged network. then restart the vm.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

1. To check server IP, type&#x20;

```bash
ip a
```

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. Pick the one in the enp0s3.
3. Open up Putty.
4. Enter the IP and password on request and the connection will start.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

5. And, we have the access.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
