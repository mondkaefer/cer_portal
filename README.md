cer_portal
==========

Slim, web-based portal to integrate other webpages into a single webpage.

The disparate webpages are pulled into the portal via an iframe and displayed under a central header and menu structure.

The state of the iframe, i.e. the loaded URL including query string and hash, is stored in the hash of the URL of the main page to enable bookmarking.
State changes to the iframe, caused by clicks on menu links from outside the iframe, by history changes using the browsers back and forward button, or by clicks on links of the page within the iframe are captured and stored.

All integrated webpages that need to be protected by Tuakiri/Shibboleth, are proxied through a "protected path" that is intercepted by Shibboleth. This configuration must be done in the proxy configuration of the hosting web server.

### Note to self:
To load pages into the iframe requested by clicks on links outside of the iframe, or by using the browsers history, a new iframe must be created every time and the old iframe must be replaced with the new iframe. 

Just setting a new src element on the old iframe causes duplication of entries in the browser history (one for the main page, one for the newly sourced element in the iframe), and makes using the browser history a rather unpleasant experience.


