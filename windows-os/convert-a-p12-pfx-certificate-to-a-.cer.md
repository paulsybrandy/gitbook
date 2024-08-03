---
description: >-
  How to convert a P12/PFX certificate to a .cer file using openssl via command
  prompt/terminal.
---

# Convert a P12/PFX Certificate to a .CER

**Use the following command to convert, using the filename with correct extension (pfx or p12) and using the directory (if you are not already in the directory the file is located in):**

`openssl pkcs12 -in [filename].pfx -clcerts -nokeys -out [filename].crt`
