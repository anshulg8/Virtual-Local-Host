# Virtual-Local-Host
Configuring sub-domains in development with http://aglh.me

Tired of having no choice but to add aliases for localhost to /etc/hosts/ every time you work on a site/app that uses sub-domains? 
Me too.

That’s why I grabbed aglh.me and made it a localhost wildcard, pointing *.aglh.me at 127.0.0.1

If you’re a rails developer, try visiting aglh.me:3000, It basically sends everything you throw at it to your localhost.

There is no HTTP server involved here at all. The DNS A record for aglh.me is 127.0.0.1, which refers to your own machine.

Note: Using this URL as a "callback url" probably won't work at all, since when Twitter/FB tries to contact aglh.me, they'll get 127.0.0.1, which refers to their own machine (not yours).
