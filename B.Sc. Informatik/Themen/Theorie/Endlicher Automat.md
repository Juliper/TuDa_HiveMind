---
title: Endlicher Automat
description: Grundlegendes Berechnungsmodell
tags:
  - theorie
---

# Endlicher Automat

Ein endlicher Automat (Finite Automaton) ist ein mathematisches Modell zur Beschreibung von Berechnungen mit endlich vielen Zuständen.

## Definition (DFA)

Ein deterministischer endlicher Automat ist ein 5-Tupel:

$$
M = (Q, \Sigma, \delta, q_0, F)
$$

| Symbol | Bedeutung |
|--------|-----------|
| $Q$ | Endliche Menge von Zuständen |
| $\Sigma$ | Eingabealphabet |
| $\delta: Q \times \Sigma \to Q$ | Übergangsfunktion |
| $q_0 \in Q$ | Startzustand |
| $F \subseteq Q$ | Akzeptierende Zustände |

## Beispiel

Automat, der Wörter mit gerader Anzahl von 1en akzeptiert:

```
     0           0
    ┌─┐         ┌─┐
    ▼ │         ▼ │
→ ((q0)) ──1──▶ (q1)
      ◀────1────
```

## DFA vs. NFA

| Eigenschaft | DFA | NFA |
|-------------|-----|-----|
| Übergänge | Eindeutig | Mehrere möglich |
| ε-Übergänge | Nein | Ja |
| Komplexität | Einfacher zu simulieren | Kompakter |
| Mächtigkeit | Gleich | Gleich |

> [!note] Äquivalenz
> Jeder NFA kann in einen äquivalenten DFA umgewandelt werden (Potenzmengenkonstruktion).

## Siehe auch

- [[Reguläre Sprachen|Reguläre Sprachen]]
- [[Aussagenlogik|Aussagenlogik]]

---

> [!abstract] Relevant für
> AFE
