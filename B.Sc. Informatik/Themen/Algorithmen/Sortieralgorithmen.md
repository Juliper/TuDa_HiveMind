---
title: Sortieralgorithmen
description: Algorithmen zum Sortieren von Daten
tags:
  - algorithmen
---

# Sortieralgorithmen

Sortieralgorithmen ordnen Elemente einer Liste nach einem Kriterium.

## Übersicht

| Algorithmus | Best | Average | Worst | Stabil | In-place |
|-------------|------|---------|-------|--------|----------|
| Bubble Sort | $O(n)$ | $O(n^2)$ | $O(n^2)$ | Ja | Ja |
| Insertion Sort | $O(n)$ | $O(n^2)$ | $O(n^2)$ | Ja | Ja |
| Merge Sort | $O(n \log n)$ | $O(n \log n)$ | $O(n \log n)$ | Ja | Nein |
| Quick Sort | $O(n \log n)$ | $O(n \log n)$ | $O(n^2)$ | Nein | Ja |
| Heap Sort | $O(n \log n)$ | $O(n \log n)$ | $O(n \log n)$ | Nein | Ja |

## Quick Sort

Divide-and-Conquer Algorithmus:

```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)
```

## Merge Sort

```python
def mergesort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left = mergesort(arr[:mid])
    right = mergesort(arr[mid:])
    return merge(left, right)
```

## Siehe auch

- [[Komplexitätsanalyse|Komplexitätsanalyse]]
- [[Rekursion|Rekursion]]

---

> [!abstract] Relevant für
> AuD
