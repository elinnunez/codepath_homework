# Project 7/8 - WordPress Vulnerabilities

## Report

### 1. Title: WordPress Version 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename (CVE-2016-7168)
  - [ ] Summary: An attacker can create a specially crafted image file name which, when uploaded in WordPress, injects malicious JavaScript code into the application.
   
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
    
  - [ ] GIF Walkthrough: <img src="wp_xss.gif" alt="Cross-Site Scripting (XSS)">
  - [ ] Steps to recreate: You need to be an admin to create a title post containing the harmful attachment name with script which is included below. Once posted, on refresh of the page an alert from the malicious script is triggered.

    `cengizhansahinsumofpwn<img src=a onerror=alert(document.cookie)>.jpg`

  - [ ] Sources Used: 
    - [Link 1](https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html)
