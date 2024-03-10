# Setting up Ubuntu Server

***

### Pre-Requisites:

1. [Virtual Box](https://www.virtualbox.org/wiki/Downloads)&#x20;
2. [Ubuntu Server ISO ](https://releases.ubuntu.com/18.04/)(It is recommended to install Ubuntu 18 if your hardware isn't latest)

***

### Configuration Steps:

1. Open Virtual Box.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. Click on New, then name the VM and add the path.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Assign Suitable memory and number of processors.
4. Assign Hardware Memory of at least 25GB so the Server functions smoothly and click finish.

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

5. Once the VM is ready, press on Start.

<figure><img src=".gitbook/assets/image (4) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

6. Once the machine is on, press on "Try or Install Ubuntu Server"

<figure><img src=".gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

7. Wait for the Installer to show up then select "English" Language.

<figure><img src=".gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

8. There is no need to update right now, so we will move on without updating.

<figure><img src=".gitbook/assets/image (7) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

9. With the keyboard layout select, press "Done"

<figure><img src=".gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure>

10. Use the Default Network Connection and press "Done"

<figure><img src=".gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>

11. There is no need to provide a proxy address.

<figure><img src=".gitbook/assets/image (10) (1) (1).png" alt=""><figcaption></figcaption></figure>

12. For the Ubuntu Archive mirror, wait for the link to be tested, then press "Done"

<figure><img src=".gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

13. Now let the VM use the entire disk (the 25GB), then press "Done"

<figure><img src=".gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

14. No need to do anything with the storage memory, just move on with "Done"

<figure><img src=".gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

15. The VM only knows about the allocated 25GB, thus we can continue to format.

<figure><img src=".gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>

16. Now set up your credentials.

<figure><img src=".gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure>

17. There is no need to upgrade to "Ubuntu Pro", directly "Continue".
18. If unselected, select the "Install OpenSSH" then press Done.

<figure><img src=".gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>

19. There is no need to install any extra dependencies right now, just click Done and wait for the installer to finish.

<figure><img src=".gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

20. &#x20;Once the installation is complete, click on "Reboot Now"

<figure><img src=".gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>

21. Once rebooted, Press Enter to unmount and continue with the server.

<figure><img src=".gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>

22. &#x20;Wait for the VM to spin up, the enter your credentials.
23. &#x20;Finally, once the finishing touches are done. The server is up and running.

<figure><img src=".gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>

24. &#x20;And that's it, this is how we setup a Ubuntu Server as a Virtual Machine.
