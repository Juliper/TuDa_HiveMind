---
title: Authentifizierung
description: Verfahren zur Identitätsprüfung
tags:
  - sicherheit
---

# Authentifizierung

Authentifizierung ist der Prozess, die Identität eines Benutzers oder Systems zu verifizieren.

## Faktoren

| Faktor | Beschreibung | Beispiel |
|--------|--------------|----------|
| Wissen | Etwas, das man weiß | Passwort, PIN |
| Besitz | Etwas, das man hat | Smartcard, Token |
| Inhärenz | Etwas, das man ist | Fingerabdruck, Gesicht |

> [!tip] Multi-Faktor-Authentifizierung (MFA)
> Kombination mehrerer Faktoren erhöht die Sicherheit erheblich.

## Passwort-Sicherheit

### Speicherung

```
Passwort ──▶ Hash(Passwort + Salt) ──▶ Speichern
```

| Element | Zweck |
|---------|-------|
| Salt | Verhindert Rainbow-Table-Angriffe |
| Slow Hash | Erschwert Brute-Force (bcrypt, Argon2) |

### Angriffe

| Angriff | Gegenmaßnahme |
|---------|---------------|
| Brute-Force | Rate-Limiting, Account-Lockout |
| Dictionary | Komplexe Passwörter |
| Phishing | 2FA, Security Keys |

## Token-basierte Authentifizierung

```
Login ──▶ Server ──▶ JWT Token ──▶ Client speichert Token
                                         │
Anfrage + Token ◀────────────────────────┘
```

## Siehe auch

- [[Verschlüsselung|Verschlüsselung]]
- [[Datenbanken|Datenbanken]]

---

> [!abstract] Relevant für
> CSS, Informationsmanagement
