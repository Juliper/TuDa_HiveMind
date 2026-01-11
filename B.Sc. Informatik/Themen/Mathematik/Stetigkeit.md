---
title: Stetigkeit
description: Definition und Arten der Stetigkeit von Funktionen
tags:
  - mathematik
---

# Stetigkeit

Eine Funktion ist stetig, wenn kleine Änderungen im Input nur kleine Änderungen im Output verursachen – intuitiv: der Graph hat keine "Sprünge".

## Definition (ε-δ)

$f$ ist stetig in $x_0$, wenn:

$$
\forall \epsilon > 0 \; \exists \delta > 0 \; \forall x: |x - x_0| < \delta \Rightarrow |f(x) - f(x_0)| < \epsilon
$$

## Definition (Folgenkriterium)

$f$ ist stetig in $x_0$ genau dann, wenn für jede Folge $(x_n)$ mit $x_n \to x_0$ gilt:

$$
\lim_{n \to \infty} f(x_n) = f(x_0)
$$

## Arten der Stetigkeit

| Art | Bedeutung |
|-----|-----------|
| Punktweise stetig | Stetig in einem Punkt $x_0$ |
| Stetig auf $[a,b]$ | Stetig in jedem Punkt des Intervalls |
| Gleichmäßig stetig | $\delta$ hängt nur von $\epsilon$ ab, nicht von $x_0$ |
| Lipschitz-stetig | $|f(x) - f(y)| \leq L \cdot |x - y|$ für eine Konstante $L$ |

## Wichtige Sätze

> [!note] Zwischenwertsatz
> Ist $f$ stetig auf $[a,b]$ und $f(a) < y < f(b)$, dann existiert ein $c \in (a,b)$ mit $f(c) = y$.

> [!note] Satz vom Maximum
> Eine stetige Funktion auf einem abgeschlossenen Intervall $[a,b]$ nimmt ihr Maximum und Minimum an.

## Siehe auch

- [[Grenzwert|Grenzwert]]
- [[Ableitung|Ableitung]]

---

> [!abstract] Relevant für
> Mathe I
