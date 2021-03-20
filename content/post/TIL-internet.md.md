---
title: "TIL Internet"
date: 2020-08-25T14:50:03+09:00
hidden: false
draft: true
tags: [TIL, Internet, Client, Server, Domain, DNS]
keywords: [Coding]
description: "note for understanding better with Egoing's Daily Coding."
slug: ""
---

## Internet?


```
sequenceDiagram
Client->>Server: Request(post)
Server->>Client: Response
```

- need 2 objects. first is Client who willing to connect at someone else, second is Server.
- The signal Client asks to Server for a data is `Request`(maybe there is `post`).
- The signal from Server that returns to Client is `Response`.
- when `Request` happens, the ip address of server must be required. The address are named as `Domain` which human can read and understand the meaning. 
- The `Domain` addresses have been registered on `DNS server` that has listed all the address and domain name. It's a server for address bridging.
- The server ip can be identified by `ping <domain name>`'s result on shell.
