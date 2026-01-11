---
title: Komplexitätsanalyse
description: Laufzeit- und Speicheranalyse von Algorithmen
tags:
  - algorithmen
---

# Komplexitätsanalyse

Die Komplexitätsanalyse bewertet die Effizienz von Algorithmen bezüglich Zeit und Speicher.

## O-Notation (Big-O)

Beschreibt die obere Schranke der Laufzeit:

$$
f(n) \in O(g(n)) \iff \exists c > 0, n_0: \forall n \geq n_0: f(n) \leq c \cdot g(n)
$$

## Komplexitätsklassen

| Notation | Name | Beispiel |
|----------|------|----------|
| $O(1)$ | Konstant | Array-Zugriff |
| $O(\log n)$ | Logarithmisch | Binäre Suche |
| $O(n)$ | Linear | Lineare Suche |
| $O(n \log n)$ | Linearithmisch | Merge Sort |
| $O(n^2)$ | Quadratisch | Bubble Sort |
| $O(2^n)$ | Exponentiell | Brute-Force TSP |

## Rechenregeln

- $O(f) + O(g) = O(\max(f, g))$
- $O(f) \cdot O(g) = O(f \cdot g)$
- $O(c \cdot f) = O(f)$ für Konstante $c$

## Weitere Notationen

| Notation | Bedeutung |
|----------|-----------|
| $\Omega(g)$ | Untere Schranke |
| $\Theta(g)$ | Exakte Schranke |
| $o(g)$ | Strikt kleiner |

## Siehe auch

- [[Sortieralgorithmen|Sortieralgorithmen]]
- [[Graphenalgorithmen|Graphenalgorithmen]]
- [[Grenzwert|Grenzwert]]

---

> [!abstract] Relevant für
> AuD, AFE
