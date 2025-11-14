---
title: "Domain Naming System"
description: ""
summary: ""
date: 2025-07-09T23:44:01+08:00
lastmod: 2025-07-09T23:44:01+08:00
weight: 209
draft: false
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### Cloudflare Tunnel

A quick way to route localhost port to public.

Steps:

1. Purchase a cloudflare domain, install cloudflare on pc

```bash
winget install --id Cloudflare.cloudflared

#  At user/.cloudflared
cloudflared --version
```

Setup credentials and configuration file. Setup tunnel from cloudflare documenations.  Connect `https://website.domainname.com` to connect to `http://localhost:8080` and `https://app.domainname.com` to connect to `http://localhost:5555` though tunnel.

```yml
tunnel: <tunnel-id>
credentials-file: <credentials-path>

ingress:
  - hostname: <website.domainname.com>
    service: http://localhost:8080
    originRequest:
      noTLSVerify: true
      connectTimeout: 30s
      httpHostHeader: localhost:8080
  - hostname: <app.domainname.com>
    service: http://localhost:5555
  - service: http_status:404
```