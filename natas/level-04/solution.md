# Natas – natas4

## Challenge Overview

In this challenge, I need to find the password for the **next level**.

When I opened the page, I saw this message:

> Access disallowed.  
> You are visiting from "" while authorized users should come only from  
> "http://natas5.natas.labs.overthewire.org/"  
>  
> Refresh page

At first, this message was confusing and a little hard for me.

---

## First Thinking

I stopped and thought about what the page was asking from me.

The message says:
- I am visiting from **empty**
- Authorized users must come from a **specific URL**

So I asked myself:
- What does “visiting from” mean?
- How does a website know where I came from?

At this point, the challenge started to feel harder than the previous ones.

---

## Trying the Refresh Button

I clicked **Refresh page**, but the same message appeared again.

It was clear that:
- Just refreshing is not enough
- The server is checking something about my request

The page wants me to **come from a specific address**, but I am not sure how to do that.

---

## Opening Inspect (Developer Tools)

I thought maybe I need to **inspect the page**.

So I:
- Right-clicked on the page
- Opened **Inspect**
- Went to the **Elements** section

I started exploring the HTML structure.

---

##
 Editing HTML in Elements

Inside the Elements panel, I tried to edit the HTML manually.

I:
- Right-clicked on an element
- Chose **Edit as HTML**
- Created an `<a>` tag
- Gave it this URL:http://natas5.natas.labs.overthewire.org

Then I clicked on that link.

---

## First Result – Not Working

When I clicked the link:
- The page opened
- But I still did not see the correct content
- The access problem was still there

## Trying Again with More Understanding
I went back to the **Elements** section again.
Once more, I edited the HTML and created a link with the required URL.
This time, when I clicked it and refreshed properly, the page behaved differently.

---

## Finding the Password

After doing this, I was finally able to see the **password** on the page.

This means the server accepted my request and showed the protected content.

---

## Final Understanding

This challenge is about **how the server checks where a request comes from**.
The page is not checking the page content — it is checking **request information**.
Even though I experimented by editing HTML, the real idea behind this level is:
- The server trusts information about the request source
- This kind of protection can be bypassed

---

## Lessons Learned

From this level, I learned:
- Websites can restrict access based on request information
- Client-side tricks (HTML editing) are not real security
- Understanding how requests work is very important
- Security checks based only on request source are weak
- Each Natas level becomes harder and requires deeper thinking

---

## Personal Reflection
This level was harder for me than the previous ones.
But it helped me:
- Think more deeply
- Be patient
- Not give up when the solution is not clear at first
I am solving these challenges to improve my **security mindset**, not just to get passwords.

---

name: natas5,
password:password:0n35PkggAPm2zbEpOU802c0x0Msn1ToK

**Author:** Layla wakily