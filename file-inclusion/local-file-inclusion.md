## Local File Inclusion (LFI)

## Overview

Local File Inclusion allows anyone to read files that exist on the same server. This can lead to disclosure of sensitive information such as user accounts, configuration files or system paths.

---

## Validation

A file inclusion vulnerability was identified through a URL parameter used by the application. By modifying the parameter value it was possible to include system files provided by DVWA. A file containing user information and system paths was accessed, demonstrating that the application did not properly restrict which files could be included. As a result, sensitive information stored on the server was disclosed.

---
