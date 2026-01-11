---
title: Ableitung
description: Definition und Rechenregeln der Ableitung
tags:
  - mathematik
---

# Ableitung

Die Ableitung beschreibt die momentane Änderungsrate einer Funktion – geometrisch die Steigung der Tangente.

## Definition

$$
f'(x_0) = \lim_{h \to 0} \frac{f(x_0 + h) - f(x_0)}{h}
$$

Alternative Schreibweisen: $\frac{df}{dx}$, $\dot{f}$, $Df$

## Ableitungsregeln

| Regel | Formel |
|-------|--------|
| Konstante | $(c)' = 0$ |
| Potenz | $(x^n)' = n \cdot x^{n-1}$ |
| Summe | $(f + g)' = f' + g'$ |
| Produkt | $(f \cdot g)' = f' \cdot g + f \cdot g'$ |
| Quotient | $\left(\frac{f}{g}\right)' = \frac{f' \cdot g - f \cdot g'}{g^2}$ |
| Kettenregel | $(f \circ g)'(x) = f'(g(x)) \cdot g'(x)$ |

## Wichtige Ableitungen

| $f(x)$ | $f'(x)$ |
|--------|---------|
| $e^x$ | $e^x$ |
| $\ln(x)$ | $\frac{1}{x}$ |
| $\sin(x)$ | $\cos(x)$ |
| $\cos(x)$ | $-\sin(x)$ |
| $x^n$ | $n \cdot x^{n-1}$ |

## Höhere Ableitungen

- $f''(x)$ – zweite Ableitung (Krümmung)
- $f^{(n)}(x)$ – n-te Ableitung

## Siehe auch

- [[Grenzwert|Grenzwert]]
- [[Stetigkeit|Stetigkeit]]
- [[Integral|Integral]]

---

> [!abstract] Relevant für
> Mathe I, AuD (O-Notation)
