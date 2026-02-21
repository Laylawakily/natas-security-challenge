# Natas – natas5

## Challenge Overview

After entering **natas5**, I saw this message:
> Access disallowed. You are not logged in

At first, this message confused me.
There was:
- No login form
- No username or password input
- Nothing visible to log in

So I asked myself:
> If there is no login form, how does the website know whether I am logged in or not?

---

## First Thinking

I stopped and thought about how websites usually handle login.

From my programming knowledge, I know:
- Login state is not always shown with a form
- Websites often remember login status using **browser storage**
- This information is usually saved on the client side

So I decided to check the **Developer Tools**.
## Opening Developer Tools
I opened **Inspect / Developer Tools** in the browser and went to the **Application** section.
Inside Application, I checked step by step:

###  Local Storage
- I opened Local Storage
- I did not find anything related to login

###  Session Storage
- I checked Session Storage
- There was nothing useful there either

At this point, I thought:
> If login state is not in storage, maybe it is stored somewhere else.

---

## Important Idea – Cookies
The next thing that came to my mind was **cookies**.
I know that:
- Cookies are often used to store login status
- Servers check cookies to decide if a user is logged in or not

So I opened the **Cookies** section inside Application.

---

## Inspecting Cookies
Inside Cookies, I found an interesting entry:

- **Name:** `loggedin`
- **Value:** `0`

This was a very important discovery.

I understood that:
- `loggedin = 0` probably means **not logged in**
- If the value changes, the server behavior might change too

---

## Modifying the Cookie
I clicked on the cookie value and changed it:
Then I refreshed the page.

---

## Finding the Password

After refreshing the page:
- The “Access disallowed” message disappeared
- The page showed the **password for the next level**
This confirmed that the website was trusting the cookie value.

---

## Final Understanding

This challenge was about **authentication based on cookies**.

The website:
- Did not verify login securely on the server
- Trusted a client-side cookie to decide login status
By simply changing the cookie value, I was treated as a logged-in user.

---

## Lessons Learned
From this level, I learned:
- Login status is often stored in cookies
- Client-side cookies should never be trusted for authentication
- Anyone can modify cookies using developer tools
- Security checks must always be done on the server side
- Understanding browser storage is very important in web security

---

## Personal Reflection
At first, this challenge felt confusing because there was no login form.
But step by step, by thinking like a programmer, I realized:
- Login does not always mean typing a password
- Sometimes it is just a value stored in the browser

This level helped me understand **real-world authentication mistakes**.

---
name:natas6,
password:0RoJwHdSKWFTYR5WuiAewauSuNaBXned

✍️ **Author:** Layla Wakily