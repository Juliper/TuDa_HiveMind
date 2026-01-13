---
title: Logikgatter
description: Grundbausteine digitaler Schaltungen
tags:
  - hardware
---

# Logikgatter

Logikgatter sind die Grundbausteine digitaler Schaltungen. Sie verarbeiten binäre Signale (0 und 1).

## Grundgatter

### AND (Und)

Ausgang ist 1, wenn alle Eingänge 1 sind.

| A | B | A ∧ B |
|---|---|-------|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

### OR (Oder)

Ausgang ist 1, wenn mindestens ein Eingang 1 ist.

| A | B | A ∨ B |
|---|---|-------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

### NOT (Nicht)

Invertiert den Eingang.

| A | ¬A |
|---|----|
| 0 | 1 |
| 1 | 0 |

## Zusammengesetzte Gatter

| Gatter | Funktion | Formel |
|--------|----------|--------|
| NAND | NOT AND | $\overline{A \land B}$ |
| NOR | NOT OR | $\overline{A \lor B}$ |
| XOR | Exklusiv-Oder | $A \oplus B$ |
| XNOR | Exklusiv-NOR | $\overline{A \oplus B}$ |

> [!tip] NAND ist universell
> Jede Boolesche Funktion kann nur mit NAND-Gattern realisiert werden.

## Siehe auch

- [[Flip-Flop|Flip-Flop]]
- [[Aussagenlogik|Aussagenlogik]]

---

> [!abstract] Relevant für
> Digitaltechnik, Rechnerorganisation
