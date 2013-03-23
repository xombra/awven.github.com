lightblog
=========

Why use light blog over Wordpress or Drupal?
1. It's simple
2. It doesn't need a database
4. It's lightweight
5. No installation required, just drag and drop files

Installation in 10 simple steps
------------

1. First of all get yourself a copy of the files by clicking [here (.zip)](https://github.com/SiteOctopus/Light-Blog/zipball/master) or by git cloning

2. Now you need to install the whole folder onto your *linux* webserver.
3. Make sure that there's a file called `.htaccess`. If not create one containing this code:
```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond $1 !^(index\.php)
RewriteRule ^(.*)$ index.php/$1 [L]
```

4. Now open `app/config.ini` in your favourite text editor. Change the `site.url` variable to the location of index.php. For example: `http://example.com` or `http://example.com/folder/`. Just remember to include a trailing slash

5. Change the blog info to match your blog. Now save the file back onto your webserver

6. Now open `app/views/layout.html.php`. You'll see some HTML code. Between the code `<!-- the sidebar-->` and `<!--End custom sidebar-->` you can add whatever you want. We've put a `<ul>` list in for you, but you can have anything!

7. Now create you first post using Markdown. The syntax help is [here](http://daringfireball.net/projects/markdown/syntax). You *must* begin your document with 
`#Title here`
otherwise it won't work!

8. Call your file:
	YYYY-MM-DD_a-title.md
9. Now refresh the page
10. Your blog is complete!

Credits
-------
Making light blog wouldn't have been possible without (in no particular order...)
* [PHP Markdown](https://github.com/dflydev/dflydev-markdown)
* [Composer](http://getcomposer.org/)
* [PHP RSS Writer](https://github.com/suin/php-rss-writer)
* [Dispatch](http://noodlehaus.github.com/dispatch/)

License
-------
<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/deed.en_GB"><img alt="Creative Commons Licence" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/deed.en_GB">Creative Commons Attribution-ShareAlike 3.0 Unported License</a>.