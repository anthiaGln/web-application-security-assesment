# File Upload Vulnerabilities

## Overview

File upload vulnerabilities occur when a web application does not properly validate files that were uploaded by the users. This can allow malicious files to be uploaded and executed on the server. Such vulnerabilities are considered high risk because they may lead to remote command execution, data exposure or full system compromise.

---

## Validation (Lab-Based)

The vulnerability was validated in Kali Linux using DVWA hosted on Metasploitable.
Steps to validate vulnerability:

1. Reduced the application security level to **Low** to demonstrate the impact of insufficient validation.
2. Accessed the file upload functionality in DVWA.
3. Uploaded a legitimate image file to confirm normal application behavior.
4. Identified the server-side location where uploaded files were stored.
6. Uploaded a PHP file generated for testing purposes.

The uploaded file was accessible through the web server, confirming that file type validation and execution restrictions were not properly enforced.

---

## Impact

An insecure file upload mechanism may allow an attacker to:

- Upload executable files to the server
- Achieve remote command execution
- Establish reverse connections to external systems
- Gain full control over the affected application or server
