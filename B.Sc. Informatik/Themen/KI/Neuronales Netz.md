---
title: Neuronales Netz
description: Vom Gehirn inspirierte Lernmodelle
tags:
  - ki
---

# Neuronales Netz

Künstliche neuronale Netze sind vom biologischen Gehirn inspirierte Rechenmodelle.

## Aufbau

```
Input Layer    Hidden Layer(s)    Output Layer
    ○              ○                  ○
    ○ ──────────── ○ ──────────────── ○
    ○              ○
    ○              ○
```

## Perceptron

Einfachstes Neuron:

$$
y = \sigma\left(\sum_{i=1}^{n} w_i x_i + b\right)
$$

| Symbol | Bedeutung |
|--------|-----------|
| $x_i$ | Eingaben |
| $w_i$ | Gewichte |
| $b$ | Bias |
| $\sigma$ | Aktivierungsfunktion |

## Aktivierungsfunktionen

| Funktion | Formel | Verwendung |
|----------|--------|------------|
| Sigmoid | $\frac{1}{1 + e^{-x}}$ | Binäre Klassifikation |
| ReLU | $\max(0, x)$ | Hidden Layers |
| Softmax | $\frac{e^{x_i}}{\sum_j e^{x_j}}$ | Multi-Klassen Output |

## Training

### Forward Pass
Eingabe durch Netz propagieren.

### Backpropagation
Fehler rückwärts durch Netz propagieren und Gewichte anpassen:

$$
w_{neu} = w_{alt} - \eta \cdot \frac{\partial L}{\partial w}
$$

| Symbol | Bedeutung |
|--------|-----------|
| $\eta$ | Lernrate |
| $L$ | Loss-Funktion |

## Architekturen

| Typ | Anwendung |
|-----|-----------|
| CNN | Bildverarbeitung |
| RNN/LSTM | Sequenzen, Text |
| Transformer | NLP, moderne LLMs |

## Siehe auch

- [[Maschinelles Lernen|Maschinelles Lernen]]
- [[Matrix|Matrix]]

---

> [!abstract] Relevant für
> KI
