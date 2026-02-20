
# Natas Level 0 – Writeup
# url('http://natas0.natas.labs.overthewire.org')

## Challenge Overview

This is **Level 0** of the Natas security challenges.  
The page says:

> *You can find the password for the next level on this page.*

The goal is to find the password for **natas1**.

---

## My Thought Process

At first, I stopped and thought:

- The page says the password is on this page
- But I cannot see anything directly
- So the password might be hidden

I asked myself:
> *What is the first thing I should check?*

---

## First Step – View Page Source

My first idea was to **view the page source**.

I opened **View Page Source** in the browser.

Inside the HTML source code, I found this comment:

```html
<!-- The password for natas1 is 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq -->

0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq is the password for Level 1.
Using this password, I can successfully log in to the next level.
Now I move on to Level 1, and I feel very excited to continue solving the next challenges.