# Assignment-7a
Vulnerability 1:
A comment longer than the SQL text field that stores it can lead to malformed HTML that can open up XSS vulnerabilities. 
Vulnerability type: XSS
Tested in 4.2
Patched in 4.2.1

![screenfetch](https://user-images.githubusercontent.com/98841506/162588302-eda7bbc3-96c5-45b3-8a00-aff403005cdc.gif)

Create an "" tag longer than 64k in a comment, which upon truncation renders as malformed HTML. 
View the comment to get the XSS

References: https://wpvulndb.com/vulnerabilities/7945
http://klikki.fi/adv/wordpress2.html

Vulnerability 2:
Unauthenticated Genericons Cross-Site Scripting

A leftover example file in one of the default wordpress files is vulnerable to XSS.
Tested in version: 4.2
Patched in version: 4.2.2

![2](https://user-images.githubusercontent.com/98841506/162592504-13212c73-dcd4-43fd-bca6-b621c6d4d63a.gif)

Create a malicious link using the "filter" feature of the genericons example page with XSS embedded in it for a post.

Source code: https://core.trac.wordpress.org/browser/tags/4.2/src/wp-content/themes/twentyfifteen/genericons/example.html

Reference: https://wpvulndb.com/vulnerabilities/7979

Vulnerability 3
Shortcode Tags Cross-Site Scripting
Shortcode tags can be mixed with HTML to lead to malformed HTML, bypassing KSES validation and opening up XSS. 
Tested in version:4.2
Patched in version: 4.2.5

![3](https://user-images.githubusercontent.com/98841506/162593198-c39e093c-0e7f-4045-8662-d22103313b37.gif)


Put the quotes in the message box and put HTML inside of shortcodes. Put this in a post.

Source code: https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8
Reference: https://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/

















