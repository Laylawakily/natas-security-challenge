

# Natas – natas6

## Challenge Description

In **Natas Level 6**, the goal is to find the password for **natas7**.

When I opened the page, I saw a simple input field with the label:

> **Input secret**

I tried entering random text and numbers, but every attempt returned the same message:

> Wrong secret

There was no visible hint on the page, so I needed to dig deeper.

---

## Initial Thinking

At this point, I asked myself:
- The page is clearly checking my input
- There must be a correct secret value
- Where is this secret stored?

Since previous Natas levels often hide information in the source code, my next step was obvious.

---

## Viewing the Source Code

I clicked **View Source Code** and found the following PHP code:

```php
<?
include "includes/secret.inc";

if(array_key_exists("submit", $_POST)) {
    if($secret == $_POST['secret']) {
        print "Access granted. The password for natas7 is <censored>";
    } else {
        print "Wrong secret";
    }
}
?>
 
Code Analysis
Reading the code carefully, a few important things became clear:
The page includes another file:
include "includes/secret.inc";

The variable $secret is not defined in this file, which means it must be defined inside secret.inc.
The application compares:
$secret == $_POST['secret']

So if I can discover the value of $secret, I can pass the check.
At this moment, the include statement immediately caught my attention.

Finding the Included File
From previous levels, I learned that sometimes included files are directly accessible through the browser.
So I tried opening the included file manually by appending it to the URL:
/includes/secret.inc
When I opened that path, I saw this content:
<?
$secret = "FOEIUWGHFEEUHOFUOIU";
?>

Secret Discovered
This was the key moment.
The secret value was clearly defined in the included file:
$secret = "FOEIUWGHFEEUHOFUOIU";
Now everything made sense.
Solving the Challenge
I went back to the original input form and entered the secret value:
FOEIUWGHFEEUHOFUOIU
After submitting the form, the page responded with:
Access granted. The password for natas7 is shown
This confirmed that the secret was correct and the level was successfully solved.

Lesson Learned:
Never trust that included files are hidden
Source code analysis is extremely powerful
Sensitive data should never be stored in accessible files
Always check include and require paths

name:natas7,
password:bmg8SvU1LizuWjx3y7xkNERkHxGre0GS
