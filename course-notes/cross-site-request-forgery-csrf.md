# Cross Site Request Forgery (CSRF)

Cross-Site Request Forgery (CSRF) is an attack where a malicious website tricks a user's browser into making an unintended request to a different site where the user is authenticated. This can lead to unauthorized actions being performed on behalf of the user without their knowledge or consent.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

## Example:

a CSRF token can be addded to the HTML code as a verification token.

<pre class="language-html"><code class="lang-html">&#x3C;body>
<strong>    &#x3C;form id="myForm" action="process.php" method="post">
</strong>        &#x3C;!-- CSRF Token -->
        &#x3C;input type="hidden" name="csrf_token" value="your_random_token_here">
        &#x3C;!-- Other form fields -->
        &#x3C;label for="userInput">Enter your data:&#x3C;/label>
        &#x3C;input type="text" id="userInput" name="userInput">
        &#x3C;button type="submit">Submit&#x3C;/button>
    &#x3C;/form>
&#x3C;/body>
</code></pre>

The verification code could be like:

```php
<?php
session_start();
// Validate CSRF token
if ($_POST['csrf_token'] !== $_SESSION['csrf_token']) {
    die("CSRF token validation failed. Request aborted.");
}
// Process other form data
$userInput = $_POST['userInput'];
// Your processing logic here
echo "Form submitted successfully!";
```

## Another example:

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## What to do?

* If you get a pop-up, call, spam email or any other urgent message about a virus on your computer, stop.
* Don’t click on any links or call a phone number. Don’t send any money. Don’t give anyone control of your computer.
* Microsoft does not display pop-up warnings and ask you to call a toll-free number about viruses or security problems.
* Report it at ftc.gov/complaint. Include the phone number that you were told to call. Keep your security software up to date.
* Know what it looks like so you can spot a fake. Tell someone about this scam. You might help them spot it and avoid a costly call.
