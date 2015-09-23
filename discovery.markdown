￼#Discovery

## Find the road less traveled
This means find the application (or parts of an application) less tested:

1. ^.acme.com scope is your friend
2. Find domains via Google (and others!)
  a. Can be automated well via recon-ng and other tools.
3. Port scan for obscure web servers or services (on all domains)
4. Find acquisitions and the bounty acquisition rules
  a. Google has a 6 month rule
5. Functionality changes or re-designs
6. Mobile websites
7. New mobile app versions

## ￼Tool: Recon-ng script (enumall.sh
https://github.com/jhaddix/domain

## ￼LMGTFY: Let Me GOOGLE That For You
site:paypal.com -www.paypal.com -www.sandbox
￼￼
## List of Mergers and Acquisitinos:
https://en.wikipedia.org/wiki/List_of_mergers_and_acquisitions_by_Facebook

## Port Scanning
Port scanning is not just for Netpen! A full port scan of all your new found targets will usually yield #win:

- separate webapps
- extraneous services
- Facebook had Jenkins Script console with no auth
- IIS.net had rdp open vulnerable to MS12_020

nmap -sS -A -PN -p- --script=http-title dontscanme.bro (syn scan, OS + service fingerprint, no ping, all ports, http titles)
