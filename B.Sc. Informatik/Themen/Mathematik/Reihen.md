---
title: Reihen
description: Unendliche Summen von Folgengliedern
tags:
  - mathematik
---

# Reihen

Eine Reihe ist die Summe der Glieder einer Folge.

## Definition

$$
\sum_{n=1}^{\infty} a_n = \lim_{N \to \infty} \sum_{n=1}^{N} a_n
$$

Die Partialsummen sind: $S_N = \sum_{n=1}^{N} a_n$

## Konvergenzkriterien

### Notwendiges Kriterium

$$
\sum a_n \text{ konvergiert} \Rightarrow \lim_{n \to \infty} a_n = 0
$$

> [!warning] Achtung
> Die Umkehrung gilt nicht! (Beispiel: harmonische Reihe)

### Quotientenkriterium

Falls $\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = q$:
- $q < 1$: konvergiert absolut
- $q > 1$: divergiert
- $q = 1$: keine Aussage

### Wurzelkriterium

Falls $\lim_{n \to \infty} \sqrt[n]{|a_n|} = q$:
- $q < 1$: konvergiert absolut
- $q > 1$: divergiert

## Wichtige Reihen

| Reihe | Wert |
|-------|------|
| Geometrische Reihe | $\sum_{n=0}^{\infty} q^n = \frac{1}{1-q}$ für $|q| < 1$ |
| Exponentialreihe | $\sum_{n=0}^{\infty} \frac{x^n}{n!} = e^x$ |
| Harmonische Reihe | $\sum_{n=1}^{\infty} \frac{1}{n}$ divergiert! |

## Siehe auch

- [[Folgen|Folgen]]
- [[Grenzwert|Grenzwert]]

---

> [!abstract] Relevant für
> Mathe I
