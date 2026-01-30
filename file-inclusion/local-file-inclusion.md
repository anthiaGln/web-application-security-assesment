## Local File Inclusion (LFI)

## Overview

Local File Inclusion allows anyone to read files that exist on the same server. This can lead to disclosure of sensitive information such as user accounts, configuration files or system paths.

---

## Validation

A file inclusion vulnerability was identified through a URL parameter used by the application. By modifying the parameter value it was possible to include system files provided by DVWA. A file containing user information and system paths was accessed, demonstrating that the application did not properly restrict which files could be included.

---

## Impact

A Local File Inclusion vulnerability can lead to unauthorized access to sensitive files stored on the server. More specifically anyone can :
- Read system files
- Access user account information
- Disclose sensitive data

 ---

 ## Mitigation

 To prevent Local File Inclusion vulnerabilities, the following security measures are recommended:
 
- Avoid dynamic file inclusion based on user-controlled input.
- Do not include files using values obtained directly from GET or POST parameters.
- Use static file inclusion where possible.
- Restrict file access to predefined and trusted directories only.
- Prevent access to files outside the intended web directory.

---

## Best Practice Summary

The most effective way to prevent Local File Inclusion vulnerabilities is to avoid dynamic file inclusion. Using static, hard-coded file inclusion ensures that users cannot influence which files are loaded by the application so that reduces the risk of sensitive data disclosure.
