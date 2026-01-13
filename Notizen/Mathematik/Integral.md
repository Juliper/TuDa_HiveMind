---
title: Integral
description: Definition und Berechnung von Integralen
tags:
  - mathematik
---

# Integral

Das Integral berechnet den "Flächeninhalt unter einer Kurve" – es ist die Umkehrung der Ableitung.

## Bestimmtes Integral

$$
\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i) \cdot \Delta x
$$

Geometrisch: Fläche zwischen $f(x)$ und der x-Achse im Intervall $[a,b]$.

## Unbestimmtes Integral (Stammfunktion)

$$
\int f(x) \, dx = F(x) + C \quad \text{wobei} \quad F'(x) = f(x)
$$

## Hauptsatz der Differential- und Integralrechnung

$$
\int_a^b f(x) \, dx = F(b) - F(a)
$$

## Integrationsregeln

| Regel | Formel |
|-------|--------|
| Linearität | $\int (af + bg) = a\int f + b\int g$ |
| Partielle Integration | $\int u \cdot v' = u \cdot v - \int u' \cdot v$ |
| Substitution | $\int f(g(x)) \cdot g'(x) \, dx = \int f(u) \, du$ |

## Wichtige Integrale

| $f(x)$ | $\int f(x) \, dx$ |
|--------|-------------------|
| $x^n$ | $\frac{x^{n+1}}{n+1} + C$ (für $n \neq -1$) |
| $\frac{1}{x}$ | $\ln|x| + C$ |
| $e^x$ | $e^x + C$ |
| $\sin(x)$ | $-\cos(x) + C$ |
| $\cos(x)$ | $\sin(x) + C$ |

## Siehe auch

- [[Ableitung|Ableitung]]
- [[Wahrscheinlichkeit|Wahrscheinlichkeit]]

---

> [!abstract] Relevant für
> Mathe I, PMI
