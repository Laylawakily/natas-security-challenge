# Natas - natas8 

you arrive at **Natas 7** (from **OverTheWire**)
You only see two links:
* **Home**
* **About**

At first, it looks like there is nothing useful.
But you did the **correct thing**: you checked **View Source**.

---

## View Source — The Important Hint
Inside the page source, you see this comment:
<!-- hint: password for webuser natas8 is in /etc/natas_webpass/natas8 -->

### What does this mean?

This message is telling us:
* The **password for the next level (natas8)**
* Is stored inside this file on the server:
```
/etc/natas_webpass/natas8
```

So now the question is:
> How can we read this file from the website?

---

## Observing the URL Behavior

When you click **Home** or **About**, you notice something important in the URL.
Example:
```
index.php?page=home
index.php?page=about
```

This tells us something critical:
The website loads pages using the **`page` parameter**.
That means the PHP code is probably doing something like:

---

##  The Key Idea (Your Thinking Was Correct!)
You asked yourself:
> “If `page` loads a file, what if I give it a file path instead?”
So instead of:
page=home, You try: page=/etc/natas_webpass/natas8


## The Exploit (Local File Inclusion)

Final URL
http://natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8

### What happens?
- The server **includes and prints the file**
- The file contains **only the password**
- The password for **natas8** appears on the page

**Success! You solved Natas 7**
##  Why This Works
This is a **very real security bug** in real websites.

## Important Note (For You)
You are:
* Reading hints correctly
* Understanding include logic
* Using paths intelligently
* Thinking like a **real security learner**

name:natas8,
password:xcoXLmzMkoIP9D7hlgPlh9XD7OgLAe5Q