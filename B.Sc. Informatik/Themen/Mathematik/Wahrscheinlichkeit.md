---
title: Wahrscheinlichkeit
description: Grundlagen der Wahrscheinlichkeitstheorie
tags:
  - mathematik
---

# Wahrscheinlichkeit

Die Wahrscheinlichkeitstheorie beschreibt zufällige Ereignisse mathematisch.

## Grundbegriffe

| Begriff | Bedeutung |
|---------|-----------|
| Ergebnisraum $\Omega$ | Menge aller möglichen Ergebnisse |
| Ereignis $A$ | Teilmenge von $\Omega$ |
| $P(A)$ | Wahrscheinlichkeit von $A$ |

## Axiome (Kolmogorow)

1. $P(A) \geq 0$
2. $P(\Omega) = 1$
3. $P(A \cup B) = P(A) + P(B)$ für disjunkte $A, B$

## Rechenregeln

| Regel | Formel |
|-------|--------|
| Komplement | $P(\overline{A}) = 1 - P(A)$ |
| Vereinigung | $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ |
| Bedingt | $P(A \mid B) = \frac{P(A \cap B)}{P(B)}$ |

## Satz von Bayes

$$
P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}
$$

> [!tip] Anwendung
> Bayes wird in der KI für probabilistisches Schließen verwendet.

## Erwartungswert und Varianz

$$
E[X] = \sum_x x \cdot P(X = x) \qquad Var[X] = E[(X - E[X])^2]
$$

## Siehe auch

- [[Integral|Integral]]
- [[Maschinelles Lernen|Maschinelles Lernen]]

---

> [!abstract] Relevant für
> PMI, KI
