# Integration of components

1. Open Windows Services by searching Services in Windows search bar.
2. Open it as administrator.
3. Find Splunk Forwarder and Restart.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

If Restart fails, then right click and press Start.

4. Go to the main Dashboard and click on "Search and Reporting"

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

This is the page.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

5. Click on Data Summary.
6. And thats it. Its working

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

The 3 data sources we enabled:

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Example Log:

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Maintaining IP Address Connections

Since our IP address changes every 24 hours, what we can do is firstly note our server IP address

then go the directory `C:\Program Files\SplunkUniversalForwarder\etc\System\local`

and then update the server IP in the `outputs.conf` and `deploymentclient.conf` files.

Finally, restart Splunk Forwarder.
