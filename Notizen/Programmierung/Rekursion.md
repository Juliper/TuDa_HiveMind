---
title: Rekursion
description: Funktionen die sich selbst aufrufen
tags:
  - programmierung
---

# Rekursion

Eine Funktion ist rekursiv, wenn sie sich selbst aufruft. Jede Rekursion braucht einen Basisfall um zu terminieren.

## Aufbau

```java
public int fakultaet(int n) {
    if (n <= 1) return 1;          // Basisfall
    return n * fakultaet(n - 1);   // Rekursiver Aufruf
}
```

## Arten

| Art | Beschreibung |
|-----|--------------|
| Lineare Rekursion | Ein rekursiver Aufruf pro Durchlauf |
| Baumrekursion | Mehrere rekursive Aufrufe (z.B. Fibonacci) |
| Endrekursion | Rekursiver Aufruf ist letzte Operation |

## Endrekursion (Tail Recursion)

Kann vom Compiler optimiert werden:

```java
public int fakultaetTail(int n, int acc) {
    if (n <= 1) return acc;
    return fakultaetTail(n - 1, n * acc);  // Endrekursiv
}
```

## Rekursion vs. Iteration

| Rekursion | Iteration |
|-----------|-----------|
| Eleganter für baumartige Strukturen | Oft effizienter (kein Stack-Overhead) |
| Kann Stack Overflow verursachen | Konstanter Speicherverbrauch |

## Siehe auch

- [[Sortieralgorithmen|Sortieralgorithmen]] (Merge Sort, Quick Sort)
- [[Graphenalgorithmen|Graphenalgorithmen]] (DFS)

---

> [!abstract] Relevant für
> FOP, AuD
