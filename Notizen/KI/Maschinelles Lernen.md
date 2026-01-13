---
title: Maschinelles Lernen
description: Algorithmen die aus Daten lernen
tags:
  - ki
---

# Maschinelles Lernen

Maschinelles Lernen (ML) ermöglicht Computern, aus Daten zu lernen, ohne explizit programmiert zu werden.

## Lernparadigmen

| Paradigma | Beschreibung | Beispiel |
|-----------|--------------|----------|
| Supervised | Mit gelabelten Daten | Spam-Erkennung |
| Unsupervised | Ohne Labels | Clustering |
| Reinforcement | Durch Belohnung/Bestrafung | Spiele-KI |

## Supervised Learning

### Klassifikation

Diskrete Labels vorhersagen.

| Algorithmus | Eigenschaften |
|-------------|---------------|
| k-NN | Einfach, keine Trainingsphase |
| Decision Tree | Interpretierbar |
| SVM | Gut bei hochdimensionalen Daten |
| Random Forest | Ensemble, robust |

### Regression

Kontinuierliche Werte vorhersagen.

$$
y = w_0 + w_1 x_1 + w_2 x_2 + \ldots + w_n x_n
$$

## Bewertung

| Metrik | Formel |
|--------|--------|
| Accuracy | $\frac{TP + TN}{TP + TN + FP + FN}$ |
| Precision | $\frac{TP}{TP + FP}$ |
| Recall | $\frac{TP}{TP + FN}$ |
| F1-Score | $2 \cdot \frac{Precision \cdot Recall}{Precision + Recall}$ |

## Overfitting vs. Underfitting

| Problem | Ursache | Lösung |
|---------|---------|--------|
| Overfitting | Modell zu komplex | Regularisierung, mehr Daten |
| Underfitting | Modell zu einfach | Komplexeres Modell |

## Siehe auch

- [[Neuronales Netz|Neuronales Netz]]
- [[Wahrscheinlichkeit|Wahrscheinlichkeit]]
- [[Matrix|Matrix]]

---

> [!abstract] Relevant für
> KI, PMI
