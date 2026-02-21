# Natas – natas2

##  Challenge Overview

This challenge requires finding the password for **natas3**.

When I opened the page for this level, it only displayed the following message:

> There is nothing on this page.

At first glance, the page looked empty and confusing.

---

## My Thinking Process

From previous levels, I learned an important rule in Natas challenges:

> If the page says *“You can find the password for the next level on this page”*,  
> then the password **must exist somewhere**, even if it is not visible.

So I asked myself:
- Where could the password be hidden this time?
- Why is nothing directly shown on the page?

---

## Checking the Page Source

I opened **View Page Source** to inspect the HTML code
Index of /files

pixel.png
users.txt
I opened the file:

users.txt.

Unlike earlier levels, I did **not** find any comment containing a password.

Instead, I noticed this line:

```html
<img src="files/pixel.png">

If the browser can load a file from /files, maybe I can access that directory directly.
Index of /files
pixel.png
users.txt

I opened the file:
users.txt
natas3:3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH


Among them was the password for natas3.