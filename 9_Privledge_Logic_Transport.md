# ￼Privilege, Transport, Logic

## Privilege

Often logic, priv, auth bugs are blurred.

Testing user priv:
- admin has power
- peon has none
- peon can use function only meant for admin

## More Privilege

- Find site functionality that is restricted to certain user types
- Try accessing those functions with lesser/other user roles
- Try to directly browse to views with sensitive information as a lesser priv user

Autorize Burp plugin is pretty neat [here] (https://github.com/Quitten/Autorize).

## Common Functions or Views
￼
- Add user function
- Delete user function
- start project / campaign / etc function
- change account info (pass, CC, etc) function
- customer analytics view
- payment processing view
- any view with PII

## ￼Insecure direct object references

IDORs are common place in bounties, and hard to catch with scanners.

Find *any and all* UIDs
- increment
- decrement
- negative values
- Attempt to perform sensitive functions substituting another UID
  - change password
  - forgot password
  - admin only functions

Common Functions , Views, or Files:
- Everything from the CSRF Table, trying cross account attacks
- Sub: UIDs, user hashes, or emails
- Images that are non-public
- Receipts
- Private Files (pdfs, ++)
- Shipping info & Purchase Orders
- Sending / Deleting messages

## Transport

Most security concerned sites will enable HTTPs. It’s your job to ensure they’ve done it *EVERYWHERE*. Most of the time they miss something.

Examples:
- Sensitive images transported over HTTP
- Analytics with session data / PII leaked over HTTP

[ForceSSL] (https://github.com/arvinddoraiswamy/mywebappscripts/tree/master/ForceSSL)

## Business Logic Flaws
Logic flaws that are tricky, mostly manual:
- substituting hashed parameters
- step manipulation
- use negatives in quantities
- authentication bypass
- application level DoS
- Timing attacks
