# Cross Site Scripting

Cross-site scripting occurs when an attacker injects malicious scripts into a web application, which then gets executed by the user's browser.

This can lead to various security risks, including the theft of sensitive information, session hijacking, or defacement of websites.

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

To prevent cross-site scripting attacks, web developers should implement proper input validation, output encoding, and use secure coding practices.

## Example:

Assume the following HTML code:

```html
<form id="myForm">
    <label for="userInput">Enter your name:</label>
    <input type="text" id="userInput" name="userInput">
    <button type="button" onclick="submitForm()">Submit</button>
</form>
```

To Sanitize this, the following code can be used:

<pre class="language-javascript"><code class="lang-javascript">&#x3C;div id="outputContainer">&#x3C;/div>
&#x3C;script>
function submitForm() {
<strong>    var userInput = document.getElementById('userInput').value;
</strong>    // Sanitize user input (replace "&#x3C;" and ">" characters)
    userInput = userInput.replace(/&#x3C;/g, "&#x26;lt;").replace(/>/g, "&#x26;gt;");
    // Display sanitized input
<strong>    var outputContainer = document.getElementById('outputContainer');
</strong>    outputContainer.innerHTML = "&#x3C;p>Your sanitized input: " + userInput + "&#x3C;/p>";
}
&#x3C;/script>
</code></pre>

The submitForm function is called when the user clicks the "Submit" button. The function retrieves the user input, sanitizes it by replacing < and > characters with their HTML entities (\&gt and \&lt), and then displays the sanitized input on the page.
