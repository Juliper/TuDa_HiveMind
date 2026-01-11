---
title: Verschlüsselung
description: Grundlagen der Kryptographie
tags:
  - sicherheit
---

# Verschlüsselung

Verschlüsselung schützt Daten vor unbefugtem Zugriff durch mathematische Transformation.

## Symmetrische Verschlüsselung

Gleicher Schlüssel für Ver- und Entschlüsselung.

```
Klartext ──[Schlüssel K]──▶ Chiffrat ──[Schlüssel K]──▶ Klartext
```

| Algorithmus | Typ | Schlüssellänge |
|-------------|-----|----------------|
| AES | Block | 128/192/256 Bit |
| ChaCha20 | Stream | 256 Bit |
| 3DES | Block | 168 Bit |

> [!warning] Problem
> Wie tauscht man den Schlüssel sicher aus?

## Asymmetrische Verschlüsselung

Schlüsselpaar: öffentlicher und privater Schlüssel.

```
Klartext ──[Public Key]──▶ Chiffrat ──[Private Key]──▶ Klartext
```

| Algorithmus | Basis |
|-------------|-------|
| RSA | Faktorisierung |
| ECC | Elliptische Kurven |
| Diffie-Hellman | Diskreter Logarithmus |

## Hashfunktionen

Einweg-Funktionen für Integrität:

| Eigenschaft | Bedeutung |
|-------------|-----------|
| Einweg | Nicht umkehrbar |
| Kollisionsresistent | Schwer zwei Inputs mit gleichem Hash zu finden |

Beispiele: SHA-256, SHA-3, BLAKE3

## Siehe auch

- [[Authentifizierung|Authentifizierung]]
- [[Matrix|Matrix]] (Kryptographie)
- [[TCP-IP|TCP/IP]] (TLS)

---

> [!abstract] Relevant für
> CSS, Computernetze
