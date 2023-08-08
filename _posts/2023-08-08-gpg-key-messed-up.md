---
title: My GPG key got messed up
category: Development
tags: gnupg key github git
---

Find out how my recent commits this week were unverified, lol.

<!-- more -->

So, last month I made a brand new email adddress and a Google account. I have already linked my active accounts to this new email address. But there's one thing I forgot to change, my GPG key and it was a big mistake.

## Changing my key's email address
I used Git Bash to open `gnupg`, edited my GPG key, and in the first minutes I've been wandering around where to change the email address for GPG keys. Heck, I even googled it because I was too dumb to look. And, that's where I realized that you can't change an email address on a key, but rather to create another user ID for the key to have the new email address in it.

Without any doubt, I created a new user ID using the `adduid` command, put the new email address, then boom! Problem solved.

But you know what's the most dumbest thing I've done after creating a new user ID? I deleted it. (dumb)

## A new problem arises
Few weeks after my GPG key was edited, I started to notice on my active repositories (even this site) that my commits were marked as *unverified*. Hmmm, what could it be causing to fail verification?

![Unverified!](/assets/img/gpg-key-messed-up_unverified.png)
<small>Notice how the commits were marked as "Unverified".</small>

## Figuring out the problem
Immediately after this, I compared the key that was set onto my Git config to sign commits and the one from GnuPG, but no luck. They are the same key.

I guessing that it was on GitHub, and I finally figured out the problem. (hopefully)

GitHub was still using the old email address that I put in the same GPG key:

![Different Email](/assets/img/gpg-key-messed-up_email.png)
<small>Shouldn't had to use the new email address.</small>

## Solution
Then, I went to Git Bash again to open `gnupg`, edited the key, used `uid`, `deluid`, and `adduid` to select, delete, and create new user IDs. Now, the GPG key would look like this:

![Fixed](/assets/img/gpg-key-messed-up_fixed.png)
<small>New email address is no more, embrace the old one.</small>

After I made these changes, new commits would now be marked as *verified.*

## Conclusion
Next time, if you decide to change your primary email address, don't replace your GPG key's email address. Otherwise you'll end up in the same way as me.

Anyways, bye for now!