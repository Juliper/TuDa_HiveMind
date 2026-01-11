---
title: Graphenalgorithmen
description: Algorithmen auf Graphen
tags:
  - algorithmen
---

# Graphenalgorithmen

Graphen bestehen aus Knoten (Vertices) und Kanten (Edges). Graphenalgorithmen lösen Probleme auf diesen Strukturen.

## Darstellung

| Art | Speicher | Kantenzugriff |
|-----|----------|---------------|
| Adjazenzmatrix | $O(V^2)$ | $O(1)$ |
| Adjazenzliste | $O(V + E)$ | $O(V)$ |

## Traversierung

### Breitensuche (BFS)

Besucht Knoten schichtweise. Nutzt eine Queue.

```python
def bfs(graph, start):
    visited = set()
    queue = [start]
    while queue:
        node = queue.pop(0)
        if node not in visited:
            visited.add(node)
            queue.extend(graph[node])
    return visited
```

**Anwendung:** Kürzeste Wege (ungewichtet)

### Tiefensuche (DFS)

Geht so tief wie möglich. Nutzt Stack/Rekursion.

```python
def dfs(graph, node, visited=None):
    if visited is None:
        visited = set()
    visited.add(node)
    for neighbor in graph[node]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)
    return visited
```

**Anwendung:** Zykluserkennung, Topologische Sortierung

## Kürzeste Wege

| Algorithmus | Gewichte | Komplexität |
|-------------|----------|-------------|
| BFS | Ungewichtet | $O(V + E)$ |
| Dijkstra | Positiv | $O((V + E) \log V)$ |
| Bellman-Ford | Beliebig | $O(V \cdot E)$ |

## Siehe auch

- [[Komplexitätsanalyse|Komplexitätsanalyse]]
- [[Rekursion|Rekursion]] (DFS)

---

> [!abstract] Relevant für
> AuD, Computernetze
