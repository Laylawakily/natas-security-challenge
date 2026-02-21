# Natas – Natas1

## Challenge Overview

This is the next challenge after solving the first step.  
The page displays the message:

> You can find the password for the next level on this page.

However, an extra restriction is added:

> Right‑clicking has been blocked!

The goal is to find the password for **natas2**.

---

## My Thought Process

At first, I read the message carefully and noticed that:

- The password is still on this page
- Right‑click is disabled, so I cannot open *View Page Source* normally

I asked myself:
> *Is right‑click the only way to view the page source?*

---

## Bypassing the Restriction

Even though right‑clicking was blocked, I knew that browsers have **keyboard shortcuts**.

I used this shortcut:[ctr+u]
This opened the **page source** successfully.

---

##  Finding the Password

Inside the HTML source code, I found the following comment:

```html
<!-- The password for natas2 is TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI -->