+++
date = '2026-03-28T21:57:44+05:30'
draft = false
title = 'New variant of Redline stealer?'
+++
Earlier versions of Redline used to have consistent config decryption that is base64decode —--> xor –-> base64decode.
![redline_1](/analysis-reports-blog/images/redline_1.png)


Today I got this sample on malwarebazaar
https://bazaar.abuse.ch/sample/796b5d63c93d71012e8a8e8a7bd9e1290ca3963b7f6c78c3cdd0023cfebe9eab/
Which is said to be a Redline stealer. This time config decryption is different. 
Configuration is decrypted using simple XOR.

![redline_2](/analysis-reports-blog/images/redline_2.png)

Here is the decryption routine of the new sample.

![redline_3](/analysis-reports-blog/images/redline_3.png)

Also build Id is in plain text which earlier used to be encrypted using the same algorithm as C2.