FreshRSS is a web application. This means you'll need a web server to run it. FreshRSS requirements are really low, so it could run on most shared host servers.

You need to verify that your server can run FreshRSS before installing it. If your server has the proper requirements and FreshRSS does not work, please contact us to find a solution.

| Software    | Recommended      | Works also with               |
| ----------- | ---------------- | ----------------------------- |
| Web server  | **Apache 2**     | Nginx                         |
| PHP         | **PHP 5.3.7+**   | PHP 5.2+                      |
| PHP modules | Required: libxml, cURL, PDO_MySQL, PCRE and ctype \\ Recommanded: JSON, Zlib, mbstring, iconv, ZipArchive | |
| Database    | **MySQL 5.0.3+** | SQLite 3.7.4+                 |
| Browser     | **Firefox**      | Chrome, Opera, Safari or IE9+ |

### Important notice

FreshRSS **CAN** work with PHP 5.3.3. To do so, we are using specific functions available in the ''password_compat'' library for the form authentication. This library is compatible with PHP >= 5.3.7 but some older version include the patch.
It all depends on the distribution:

* CentOS and RHEL 6.5 are supported.
* On the other hand, **Debian with PHP 5.3.3 is not**

[For more information](https://github.com/ircmaxell/password_compat#requirements).