odt-relative-urls
=================

ngrok - converts all absolute URLs into relative URLS

This WordPress plugin converts all the absolute URLs in the front-end to relative URLs (keeps the path '/' at the beginning, so it isn't a true relative link, but from the web root base).

How does it work?
=================
When you visit a page, it will request the full HTML requesting the same page via file_get_contents(), and replace every occurrence of your domain with a slash, for example: ("http://optimiza.mx/" will be converted to "/").

It's not the best performance solution, but gets the better results; other plugins were replacing links that they shouldn't and not replacing links that they should. DON'T USE IT ON PRODUCTION WEBSITES, ONLY ON DEVELOPMENT WEBSITES.

The replacement occurs only on the front-end. The wp-admin is source code won't be modified.

Use it with ngrok
=================

This plugin can be used to tunnel a Wordpress site over ngrok.
