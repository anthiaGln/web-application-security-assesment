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

---

## Mitigation

To prevent file upload vulnerabilities, the following security measures are recommended:
- Restrict allowed file types using server-side validation
- Validate file content and MIME type, not only file extensions
- Disallow upload of executable files
- Store uploaded files outside the web root so that they will not be executed through the URL.

The most effective way to secure file upload functionality is to validate the real file type on the server side and ensure it matches the expected format, such as an image or media file. File extensions alone should not be trusted as they can be easily bypassed. 
