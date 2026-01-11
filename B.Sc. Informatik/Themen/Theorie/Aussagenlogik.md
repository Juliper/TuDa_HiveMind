---
title: Aussagenlogik
description: Grundlagen der formalen Logik
tags:
  - theorie
---

# Aussagenlogik

Die Aussagenlogik befasst sich mit Aussagen, die wahr oder falsch sein können, und deren Verknüpfungen.

## Syntax

| Symbol | Name | Bedeutung |
|--------|------|-----------|
| $\neg$ | Negation | nicht |
| $\land$ | Konjunktion | und |
| $\lor$ | Disjunktion | oder |
| $\to$ | Implikation | wenn...dann |
| $\leftrightarrow$ | Bikonditional | genau dann wenn |

## Wahrheitstabellen

### Implikation

| $A$ | $B$ | $A \to B$ |
|-----|-----|-----------|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

> [!tip] Merke
> Die Implikation ist nur falsch, wenn aus Wahrem Falsches folgt.

## Wichtige Äquivalenzen

| Name | Formel |
|------|--------|
| De Morgan | $\neg(A \land B) \equiv \neg A \lor \neg B$ |
| De Morgan | $\neg(A \lor B) \equiv \neg A \land \neg B$ |
| Kontraposition | $(A \to B) \equiv (\neg B \to \neg A)$ |
| Implikation | $(A \to B) \equiv \neg A \lor B$ |

## Normalformen

| Form | Struktur |
|------|----------|
| KNF | Konjunktion von Disjunktionen |
| DNF | Disjunktion von Konjunktionen |

## Siehe auch

- [[Logikgatter|Logikgatter]]
- [[Endlicher Automat|Endlicher Automat]]

---

> [!abstract] Relevant für
> Aussagen- und Prädikatenlogik, Digitaltechnik, MSS
