---
title: Flip-Flop
description: Speicherelemente in digitalen Schaltungen
tags:
  - hardware
---

# Flip-Flop

Ein Flip-Flop ist ein bistabiles Element, das ein Bit speichern kann. Es ist der Grundbaustein für Register und Speicher.

## RS-Flip-Flop

| S | R | Q (nächster Zustand) |
|---|---|---------------------|
| 0 | 0 | Q (unverändert) |
| 0 | 1 | 0 (Reset) |
| 1 | 0 | 1 (Set) |
| 1 | 1 | ❌ (verboten) |

## D-Flip-Flop

Übernimmt den Eingangswert D bei der Taktflanke.

| D | Q (nach Takt) |
|---|---------------|
| 0 | 0 |
| 1 | 1 |

> [!note] Taktgesteuert
> D-Flip-Flops ändern ihren Zustand nur bei steigender oder fallender Taktflanke.

## JK-Flip-Flop

Wie RS, aber J=K=1 toggelt den Ausgang.

| J | K | Q (nächster Zustand) |
|---|---|---------------------|
| 0 | 0 | Q (unverändert) |
| 0 | 1 | 0 |
| 1 | 0 | 1 |
| 1 | 1 | ¬Q (Toggle) |

## Anwendungen

- Register (Gruppe von Flip-Flops)
- Zähler
- Schieberegister
- Speicher (SRAM)

## Siehe auch

- [[Logikgatter|Logikgatter]]
- [[CPU-Architektur|CPU-Architektur]]

---

> [!abstract] Relevant für
> Digitaltechnik, Rechnerorganisation
