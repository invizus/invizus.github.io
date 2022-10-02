---
title: "How to SSL"
date: 2022-10-03T00:06:55+01:00
draft: false
---
Nowadays you do not need to know how to do SSL, because a lot of website
providers do it for you. However if you want to create SSL website yourself,
it is an easy task.

Just enabling SSL on your apache config will not work. Like, why? It is baffling!
There is a reason to that which I will discuss in other posts, but for now
lets proceed.

You would need three things for HTTPS to work.

## 1. Protocol
Obviously, your website files and a server software such as nginx or apache,
but I assume you already have all that.

First of all, we enable the SSL protocol. SSL is original protocol called
"Secure socket layer", and it went through a lot of improvements and changes,
and was discontinued. Today the TLS protocol is in use (Transport Layer Security).
Why SSL is still mentioned? Same reason why vacuums are called "hoovers" and
epinephrine is called "adrenaline".

How TLS 1.2 enabled on apache:
```
SSLProtocol             all -SSLv3 -TLSv1 -TLSv1.1
```

## 2. Ciphers
Before I wrote about insecure ciphers and which ciphers to enable, but it is better
to trust this task to robots. Well not really, but this ssl-config by Mozilla is very
good and my goto.

https://ssl-config.mozilla.org/

As computing power grew, some ciphers became weak because it became possible to crack
their mathematical algorithms. Do not use weak ciphers.

## 3. Certificate
SSL certificate is part of PKI. A certificate is a documen that contains a public key
and represents the owner information and the validity of such information. Certificate
authorities back that up by their, well, authority, and web browsers and operating systems
have necessary files to ensure this works and keep your experience secure.

For HTTPS to work, your browser and the server where the website are hosted must exchange
public keys. You have yours, and website have its own. Website's SSL cert contains such
public key.

This is a very very brief definition. But this is why self-signed certificates are not
trusted, and you should only trust one if you or someone you know created it and you are in
control of those files.

How to create self signed cert - I will post about this later.

But you can create a free SSL certificate with letsencrypt - https://letsencrypt.org

## Finishing up
Once you have your cert, navigate to Mozila's ssl configurator and generate yourself
a secure web server config.

## Testing
Test your config on websites below
- https://www.ssllabs.com/ssltest/
- https://www.sslchecker.com/certdecoder

## Random links
- https://thehackernews.com/2015/10/nsa-crack-encryption.html
- https://weakdh.org/imperfect-forward-secrecy-ccs15.pdf
- https://weakdh.org/sysadmin.html

