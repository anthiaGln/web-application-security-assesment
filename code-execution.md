# Code Execution Vulnerabilities

## Overview

Code execution vulnerabilities occur when a web application allows users to execute operating system commands on the server.
These commands may be Windows or Linux based and can lead to severe security issues.

Such vulnerabilities can be abused to obtain reverse shells or upload files to the server using system commands.

---

## Impact

If a code execution vulnerability exists, an attacker may be able to:
- Execute operating system commands on the server
- Establish a reverse shell connection
- Upload files using command-line tools such as wget

This can result in full compromise of the affected system.

---

## Mitigation

To reduce the risk of code execution vulnerabilities the following security measures are recommended:

- Avoid the use of functions that allow execution of operating system commands.
- Users should not be allowed to execute any type of code on the server.

