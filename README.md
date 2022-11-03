# WordPress-
# Project 7 - WordPress Pen Testing

Time spent: 2 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pen Testing Report

### 1. (Required) Vulnerability Name or ID

- [ ] Summary: 
  - Vulnerability types: User Numeration
  - Tested in version: 4.2
  - Fixed in version: 4.7.2
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: 
      - Attempt to log in under admin but use the wrong password, and you will get an error
      - The error will say there's an account already an account named admin
      - login with a different username, and password. You will get Lost Password?
      - Use the password finder/brute force to crack into the page

  
### 2. (Required) Vulnerability Name: Aunthenciated Cross-Site Scripting via Media File

- [ ] Summary: 
  - Vulnerability types: XSS
  - Tested in version: 4.2
  - Fixed in version: 4.7.3
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: 
      - Go to Media and upload a new file
      - After attempting to upload the file, add "filename <script>alert("Exploit 3 Successful");</script> in the description, include the quotes
      - View the attachment, and an alert will pop up for the exploit

### 3. (Required) Vulnerability Name or ID

- [ ] Summary: 
  - Vulnerability types: XSS (CVE-2015-5714)
  - Tested in version: 4.2
  - Fixed in version: 4,2,5
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: 
      - Sign in as an admin
      - Add a new post in the "Post" section
      - Change from "Visual" to "Text" editing
      - Insert the code: [caption width="1" caption='<a href="' ">]</a><a href=" onmouseover='alert("exploit!")' ">Click!</a> in text box
      - Then you will click on the underlined word

  - https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5714
