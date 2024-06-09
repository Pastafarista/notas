---
id: 1717705326-descubrimientos-de-equipos-en-la-red-local
aliases:
  - Descubrimientos de equipos en la red local
tags:
  - linux
---

# Descubrimientos de equipos en la red local

Para descubrir equipos conectados a la red local se pueden utilizar las herramientas `arp-scan` y `masscan`:

## arp-scan

```bash
arp-scan -I wlan0 --localnet --ignoredups
```

## masscan

```bash
masscan -p0-65000 192.168.1.0/24 --rate=10000
```
También se puede usar la herramienta de [[1717682023-RIJF|nmap]]
