---
title: Folgen
description: Grundlagen von Zahlenfolgen
tags:
  - mathematik
---

# Folgen

Eine Folge ist eine Abbildung von den natürlichen Zahlen in eine Menge (meist $\mathbb{R}$).

## Definition

$$
(a_n)_{n \in \mathbb{N}} = a_1, a_2, a_3, \ldots
$$

## Arten von Folgen

| Art | Definition | Beispiel |
|-----|------------|----------|
| Arithmetisch | $a_{n+1} = a_n + d$ | $1, 3, 5, 7, \ldots$ |
| Geometrisch | $a_{n+1} = a_n \cdot q$ | $1, 2, 4, 8, \ldots$ |
| Rekursiv | $a_n = f(a_{n-1}, \ldots)$ | Fibonacci |

## Eigenschaften

| Eigenschaft | Definition |
|-------------|------------|
| Beschränkt | $\exists M: |a_n| \leq M \; \forall n$ |
| Monoton wachsend | $a_{n+1} \geq a_n \; \forall n$ |
| Monoton fallend | $a_{n+1} \leq a_n \; \forall n$ |
| Konvergent | $\lim_{n \to \infty} a_n$ existiert |

## Wichtige Folgen

### Arithmetische Folge

$$
a_n = a_1 + (n-1) \cdot d
$$

Summenformel: $S_n = \frac{n}{2}(a_1 + a_n)$

### Geometrische Folge

$$
a_n = a_1 \cdot q^{n-1}
$$

Summenformel: $S_n = a_1 \cdot \frac{1 - q^n}{1 - q}$ (für $q \neq 1$)

### Fibonacci-Folge

$$
F_n = F_{n-1} + F_{n-2}, \quad F_0 = 0, F_1 = 1
$$

## Siehe auch

- [[Grenzwert|Grenzwert]]
- [[Reihen|Reihen]]
- [[Rekursion|Rekursion]]

---

> [!abstract] Relevant für
> Mathe I
