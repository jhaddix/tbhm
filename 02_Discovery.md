# Discovery

## Find the road less traveled

This means find the application (or parts of an application) less tested. In wide scoped projects the flagship application will most liekly be heavily assessed. 

- ^.acme.com scope is your friend
- Find domains via Google (and others!)
  - Can be automated well via recon-ng and other tools.
- Port scan for obscure web servers or services (on all domains)
- Find acquisitions and the bounty acquisition rules
  - Google has a 6 month rule
- Functionality changes or re-designs
- Mobile websites
- New mobile app versions
- Searching parent company by trademark or privacy policy

## ￼Tool: Recon-ng script (enumall.sh
https://github.com/jhaddix/domain

## ￼LMGTFY: Let Me GOOGLE That For You
site:paypal.com -www.paypal.com -www.sandbox
￼￼
## List of Mergers and Acquisitions:
https://en.wikipedia.org/wiki/List_of_mergers_and_acquisitions_by_Facebook

## Port Scanning
Port scanning is not just for Netpen! A full port scan of all your new found targets will usually yield #win:

- separate webapps
- extraneous services
- Facebook had Jenkins Script console with no auth
- IIS.net had rdp open vulnerable to MS12_020

``nmap -sS -A -PN -p- --script=http-title dontscanme.bro``

(syn scan, OS + service fingerprint, no ping, all ports, http titles)
