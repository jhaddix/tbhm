# Auxiliary

## The vulns formerly known as “noise”

- Content Spoofing or HTML injection
- Referer leakage
- security headers
- path disclosure
- clickjacking
- ++

## ￼How to test a web app in n minute

How can you get maximum results within a given time window?

## ￼￼Data Driven Assessment (diminishing return FTW)

1. Visit the search, registration, contact, password reset, and comment forms and hit them with your polyglot strings
2. Scan those specific functions with Burp’s built-in scanner
3. Check your cookie, log out, check cookie, log in, check cookie. Submit old
cookie, see if access.
4. Perform user enumeration checks on login, registration, and password
reset.
5. Do a reset and see if; the password comes plaintext, uses a URL based
token, is predictable, can be used multiple times, or logs you in
automatically
6. Find numeric account identifiers anywhere in URLs and rotate them for
context change
7. Find the security-sensitive function(s) or files and see if vulnerable to
non-auth browsing (idors), lower-auth browsing, CSRF, CSRF protection
bypass, and see if they can be done over HTTP.
8. Directory brute for top short list on SecLists
9. Check upload functions for alternate file types that can execute code (xss
or php/etc/etc)
