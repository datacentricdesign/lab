---
layout: post
comments: false
title:  "Generate Public/Private keys"
date:   2019-04-30 01:30:13
image: 
description: Building a small web application
main-class: 'tutorial'
color:
tags:
- tool
- SSL
categories:
twitter_text:
introduction: In order to push data on a cloud platform, you usually need to share your public key with its servers. This public key enables the server to authenticate messages coming from your device. For this we use the tool openssl.
---

On Mac, this tool is already installed. On Windows, you can download and install openssl [here](https://slproweb.com/products/Win32OpenSSL.html)

In the terminal, type in the following command to generate a private key. The private
key is saved saved in file 'private.pem'. You should keep this file secret on your computer and never share it.

```bash
openssl genrsa -out private.pem 4096
```

Then, extract the attached public key with the following command. The public key
is saved in the file 'public.pem'

```bash
openssl rsa -in private.pem -outform PEM -pubout -out public.pem
```

