# Project 7/8 - WordPress Vulnerabilities

## Report

### 1. Title: WordPress Version <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: Current versions of WordPress (Version's up to 4.2) are vulnerable to a stored XSS. An unauthenticated attacker can inject JavaScript in WordPress comments and in turn the script is triggered when the comment is viewed.
   
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
    
  - [ ] GIF Walkthrough: <img src="wp_xss.gif" alt="Cross-Site Scripting (XSS)">
  - [ ] Steps to recreate: You need an admin to approve a comment containing the embedded harmful html tag which I included below. If the comment text is long enough, it will be truncated when inserted in the database. The truncation results in malformed HTML generated on the page.

    `<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px AAAAAAAAAAAA     [64 kb] ...'></a>`

  - [ ] Sources Used: 
    - [Link 1](https://core.trac.wordpress.org/browser/tags/4.2.2/src/wp-admin/post.php)
    - [Link 2](http://klikki.fi/adv/wordpress2.html)
    - [Link 3] (https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html)
