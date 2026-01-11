---
title: Reguläre Sprachen
description: Die einfachste Klasse formaler Sprachen
tags:
  - theorie
---

# Reguläre Sprachen

Reguläre Sprachen sind die einfachste Klasse in der Chomsky-Hierarchie und werden von endlichen Automaten erkannt.

## Äquivalente Beschreibungen

Eine Sprache ist regulär, wenn sie beschrieben werden kann durch:

1. **Deterministische endliche Automaten (DFA)**
2. **Nichtdeterministische endliche Automaten (NFA)**
3. **Reguläre Ausdrücke**
4. **Reguläre Grammatiken**

## Reguläre Ausdrücke

| Ausdruck | Bedeutung |
|----------|-----------|
| $a$ | Einzelnes Zeichen |
| $\epsilon$ | Leeres Wort |
| $\emptyset$ | Leere Menge |
| $r_1 \cdot r_2$ | Konkatenation |
| $r_1 \mid r_2$ | Alternative |
| $r^*$ | Kleene-Stern (0 oder mehr) |

**Beispiel:** $(a \mid b)^* a b$ beschreibt alle Wörter über $\{a, b\}$, die auf $ab$ enden.

## Abschlusseigenschaften

Reguläre Sprachen sind abgeschlossen unter:

- Vereinigung $L_1 \cup L_2$
- Schnitt $L_1 \cap L_2$
- Komplement $\overline{L}$
- Konkatenation $L_1 \cdot L_2$
- Kleene-Stern $L^*$

## Pumping-Lemma

Zum Nachweis, dass eine Sprache **nicht** regulär ist:

> [!warning] Pumping-Lemma
> Für jede reguläre Sprache $L$ existiert $n$, sodass jedes Wort $w \in L$ mit $|w| \geq n$ zerlegbar ist in $w = xyz$ mit bestimmten Eigenschaften.

## Siehe auch

- [[Endlicher Automat|Endlicher Automat]]

---

> [!abstract] Relevant für
> AFE
