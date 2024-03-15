# Splunk Extractor

1\) Open Splunk Enterprise on host Machine.

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

2\) Click on Search and Reporting

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

3\) Click on Data Summary

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

4\) Click on Host name to view the logs.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

5\) If the logs are old, click on the \[Last 24 Hours Dropdown] and select the timeframe.

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

6\) Go to the bottom of the left bar, and Click on the Extract New Fields option.

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

7\) Select a Sample Event and Click Next

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

8\) Now, we want to target the account name from the logs so we will pick a log with account name, then we want to build a regex around it, so select regex and click next.

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

9\) Highlight the Account Name text and and click on select extractor to automatically build an extraction regex for it. Give it a name and click next.

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

10\) In the validation page, we can view the extraction results. once confirmed, click next

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

11\) Here is the save options and regex.

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

12\) Click Finish

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

13\) Click on "Explore the Fields i Just Created in Search"

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

14\) Now, In the Left Bar, Click on Account\_Name to view all the performed extractions.

<figure><img src="../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>
