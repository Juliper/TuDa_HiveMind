---
title: Grenzwert
description: Definition und Eigenschaften von Grenzwerten
tags:
  - mathematik
---

# Grenzwert

Der Grenzwert beschreibt das Verhalten einer Folge oder Funktion, wenn sich die Variable einem bestimmten Wert nähert.

## Definition (Folgengrenzwert)

Eine Folge $(a_n)$ konvergiert gegen den Grenzwert $a$, wenn:

$$
\forall \epsilon > 0 \; \exists N \in \mathbb{N} \; \forall n \geq N: |a_n - a| < \epsilon
$$

**Schreibweise:** $\lim_{n \to \infty} a_n = a$

## Definition (Funktionsgrenzwert)

$$
\lim_{x \to x_0} f(x) = L \iff \forall \epsilon > 0 \; \exists \delta > 0: |x - x_0| < \delta \Rightarrow |f(x) - L| < \epsilon
$$

## Rechenregeln

Seien $\lim_{n \to \infty} a_n = a$ und $\lim_{n \to \infty} b_n = b$:

| Regel | Formel |
|-------|--------|
| Summe | $\lim(a_n + b_n) = a + b$ |
| Produkt | $\lim(a_n \cdot b_n) = a \cdot b$ |
| Quotient | $\lim\frac{a_n}{b_n} = \frac{a}{b}$ (falls $b \neq 0$) |

## Wichtige Grenzwerte

$$
\lim_{n \to \infty} \frac{1}{n} = 0 \qquad \lim_{n \to \infty} \sqrt[n]{n} = 1 \qquad \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e
$$

## Siehe auch

- [[Folgen|Folgen]]
- [[Stetigkeit|Stetigkeit]]
- [[Ableitung|Ableitung]]
- [[Komplexitätsanalyse|Komplexitätsanalyse]]

---

> [!abstract] Relevant für
> Mathe I, Mathe II
