# Mapping

## ￼Mapping Tips:
- Google
- Smart* Directory Brute Forcing
  - RAFT lists (included in Seclists)
  - SVN Digger (included in Seclists)
  -  Git Digger
- Platform Identification:
  - Wapplyzer (Chrome)
  - Builtwith (Chrome)
  - retire.js (cmd-line or Burp)
  - Check CVE’s
- Auxiliary
  - WPScan
  -CMSmap

##￼ Directory Bruteforce Workflow
After bruteforcing look for other status codes indicating you are denied or require auth then append list there to test for misconfigured access control.

Example:

````
GET http://www.acme.com - 200
GET http://www.acme.com/backlog/ - 404
GET http://www.acme.com/controlpanel/ - **401 hmm.. ok**
GET http://www.acme.com/controlpanel/[bruteforce here now]
````

## ￼￼Mapping/Vuln Discovery using OSINT
Find previous/existing problem:
- Xssed.com
- Reddit XSS - /r/xss
- Punkspider
- xss.cx
- xssposed.org
- twitter searching

Issues might already reported but use the flaw area and injection type to guide you to further injections or filter bypass

## ￼New Project: Maps
New OSINT/Mapping project
- 250+ bounty programs
- Crawl
- DNS info + bruteforce
- Bounty metadata (links, rewards, scope)
- API -> Intrigue

https://github.com/bugcrowdlabs/maps

### ￼Using the Maps Project: Crawling
Using + Ruby + Anemone + JSON + Grep

````
$cat test_target_json.txt | grep redirect

https://test_target/redirect/?url=http://twitter.com
https://test_target/redirect/?url=http://facebook.com/...
https://test_target/redirect/?url=http://pinterest.com/...
````


## New Tool: Intrigue
OSINT framework, simple to integrate. Features like:
- DNS Subdomain Brute force
- Web Spider
- Nmap Scan
- etc
Code @ http://github.com/intrigueio/intrigue-core


￼
