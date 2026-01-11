---
title: Matrix
description: Grundlagen der Matrizenrechnung
tags:
  - mathematik
---

# Matrix

Eine Matrix ist ein rechteckiges Schema von Zahlen, das für lineare Abbildungen und Gleichungssysteme verwendet wird.

## Definition

Eine $m \times n$-Matrix:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

## Operationen

### Addition/Subtraktion

Elementweise für Matrizen gleicher Dimension.

### Multiplikation

$(A \cdot B)_{ij} = \sum_{k=1}^{n} a_{ik} \cdot b_{kj}$

> [!warning] Achtung
> Matrixmultiplikation ist **nicht** kommutativ: $A \cdot B \neq B \cdot A$

## Spezielle Matrizen

| Typ | Eigenschaft |
|-----|-------------|
| Einheitsmatrix $I$ | $A \cdot I = A$ |
| Nullmatrix | Alle Einträge 0 |
| Diagonalmatrix | Nur Diagonale ≠ 0 |
| Symmetrisch | $A = A^T$ |
| Orthogonal | $A^T = A^{-1}$ |

## Determinante

Für $2 \times 2$:

$$
\det \begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc
$$

## Siehe auch

- [[Neuronales Netz|Neuronales Netz]]
- [[Verschlüsselung|Verschlüsselung]]

---

> [!abstract] Relevant für
> Mathe II, KI, CSS (Kryptographie)
