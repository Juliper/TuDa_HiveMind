---
title: TCP/IP
description: Grundlagen des Internet-Protokollstapels
tags:
  - netzwerke
---

# TCP/IP

TCP/IP ist die Protokollfamilie, die das Internet antreibt.

## Schichtenmodell

| Schicht | Protokolle | Funktion |
|---------|------------|----------|
| Anwendung | HTTP, SMTP, DNS | Anwendungsdaten |
| Transport | TCP, UDP | Ende-zu-Ende-Kommunikation |
| Internet | IP, ICMP | Routing |
| Netzzugang | Ethernet, WiFi | Physische Übertragung |

## TCP vs. UDP

| Eigenschaft | TCP | UDP |
|-------------|-----|-----|
| Verbindung | Ja (3-Way-Handshake) | Nein |
| Zuverlässig | Ja | Nein |
| Reihenfolge | Garantiert | Nicht garantiert |
| Overhead | Hoch | Niedrig |
| Anwendung | Web, E-Mail | Streaming, Gaming |

## TCP 3-Way-Handshake

```
Client              Server
   │                   │
   │──── SYN ─────────▶│
   │◀─── SYN+ACK ──────│
   │──── ACK ─────────▶│
   │                   │
   │   Verbindung      │
   │   hergestellt     │
```

## IP-Adressierung

| Version | Format | Beispiel |
|---------|--------|----------|
| IPv4 | 32 Bit | 192.168.1.1 |
| IPv6 | 128 Bit | 2001:db8::1 |

### Subnetting

CIDR-Notation: `192.168.1.0/24` = 256 Adressen

## Siehe auch

- [[Verschlüsselung|Verschlüsselung]] (TLS)
- [[Graphenalgorithmen|Graphenalgorithmen]] (Routing)

---

> [!abstract] Relevant für
> Computernetze, CSS
