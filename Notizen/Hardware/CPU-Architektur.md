---
title: CPU-Architektur
description: Aufbau und Funktionsweise eines Prozessors
tags:
  - hardware
---

# CPU-Architektur

Die CPU (Central Processing Unit) ist das Herzstück eines Computers und führt Befehle aus.

## Komponenten

```
┌─────────────────────────────────────┐
│              CPU                     │
│  ┌─────────┐  ┌─────────────────┐   │
│  │ Steuer- │  │     ALU         │   │
│  │  werk   │  │ (Rechenwerk)    │   │
│  └─────────┘  └─────────────────┘   │
│  ┌─────────────────────────────┐    │
│  │       Register              │    │
│  └─────────────────────────────┘    │
└─────────────────────────────────────┘
```

| Komponente | Funktion |
|------------|----------|
| Steuerwerk | Holt und dekodiert Befehle |
| ALU | Führt arithmetische/logische Operationen aus |
| Register | Schneller Zwischenspeicher |

## Befehlszyklus

1. **Fetch** – Befehl aus Speicher holen
2. **Decode** – Befehl dekodieren
3. **Execute** – Befehl ausführen
4. **Writeback** – Ergebnis speichern

## Architekturen

| Architektur | Eigenschaften |
|-------------|---------------|
| CISC | Komplexe Befehle, weniger Code |
| RISC | Einfache Befehle, schnellere Ausführung |
| Harvard | Getrennte Speicher für Code und Daten |
| Von-Neumann | Gemeinsamer Speicher |

## Pipelining

Mehrere Befehle werden parallel in verschiedenen Phasen bearbeitet:

```
Zeit  →  1   2   3   4   5   6
Befehl 1: F - D - E - W
Befehl 2:     F - D - E - W
Befehl 3:         F - D - E - W
```

## Siehe auch

- [[Flip-Flop|Flip-Flop]] (Register)
- [[Logikgatter|Logikgatter]] (ALU)

---

> [!abstract] Relevant für
> Rechnerorganisation, Parallele Programmierung
