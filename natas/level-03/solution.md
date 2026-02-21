# Natas – natas3

## Challenge Overview

In this challenge, I need to find the password for **natas4**.

When I opened the **natas3** page, I only saw this message:

> There is nothing on this page

At first, this message was confusing, because it looked like there was nothing to interact with.

---

## First Thoughts

I stopped and thought carefully.

From previous Natas levels, I learned an important rule:

> If the challenge says the password is on this page, then it **must exist somewhere**, even if it is not visible.

So I asked myself:
- Why does it say “There is nothing on this page”?
- Is something hidden again?
- Is the page trying to mislead me?

---

## Checking the Page Source

The next logical step was to check the **page source**.

When I opened *View Page Source*, I found this comment:

```html
<!-- No more information leaks!! Not even Google will find it this time... -->
 I focused on this part:
Not even Google will find it this time

# Thinking About Google
I asked myself:
How does Google find pages?
What tells Google which pages to index or ignore?
As a programmer, I remembered a very important file used on websites:
robots.txt
I know that:
robots.txt is a plain text file
It is placed in the root directory of a website
It tells search engines (like Googlebot) which paths they should not crawl
It is commonly used for SEO, not for security

# Checking robots.txt
I decided to manually open the robots.txt file of the website:
http://natas3.natas.labs.overthewire.org/robots.txt
The content of the file was:
User-agent: *
Disallow: /s3cr3t/
This was a very clear hint.

It showed that:There is a directory named /s3cr3t/, Google is told not to crawl it
But this does not mean users cannot access it
Instead of robots.txt, I directly wrote the hidden path in the browser URL:
http://natas3.natas.labs.overthewire.org/s3cr3t/
Finding the Password: I opened the file: users.txt
## Final Result
The password for natas4 was stored in a hidden directory that was:
- Mentioned inside robots.txt
- Hidden from search engines, not from users
- Publicly accessible without authentication

name: natas4,
password:QryZXc2e0zahULdHrtHxzyYkj59kUxLQ