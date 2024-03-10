---
description: Set this up on VM
---

# Splunk Forwarder



1. Launch the Installer and Accept the License Agreement.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

2. Enter your credentials.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

3. Enter the IP address of the machine where Splunk is being installed, let the default port be the used one.

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

4. Use the same IP for the reciever Index and the default port of that.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

5. Click on Next then Install.
6. Wait for the Installer to Finish.
7. Then Go to `C:\Program Files\SplunkUniversalForwarder\etc\apps`
8. Paste the `Splunk_TA_Windows` File from the tar zip file.
9. Now go to `C:\Program Files\SplunkUniversalForwarder\etc\apps\Splunk_TA_windows\default` and copy the file `inputs.conf` and paste it somewhere outside`.`
10. Open the file with notepad
11. We need three types of logs, System, Security and Application, so we will set their disabled value to 0 and renderXml to false.

```
###### OS Logs ######
[WinEventLog://Application]
disabled = 0
start_from = oldest
current_only = 0
checkpointInterval = 5
renderXml=false

[WinEventLog://Security]
disabled = 0
start_from = oldest
current_only = 0
evt_resolve_ad_obj = 1
checkpointInterval = 5
blacklist1 = EventCode="4662" Message="Object Type:(?!\s*groupPolicyContainer)"
blacklist2 = EventCode="566" Message="Object Type:(?!\s*groupPolicyContainer)"
renderXml=false

[WinEventLog://System]
disabled = 0
start_from = oldest
current_only = 0
checkpointInterval = 5
renderXml=false
```

12. Go the Directory `C:\Program Files\SplunkUniversalForwarder` and create a folder named local.
13. Paste the inputs.conf file in there.
14. Click on settings, then forwarding and recieving

    <figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

    15\) Click on Add new in recieving data.

    <figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

    16\) Set the default port AKA 9997

    <figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

