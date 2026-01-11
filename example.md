---
title: Beispiel Notiz
description: Vorlage und Syntax-Referenz für Hive Mind Notizen
aliases:
  - Vorlage
  - Template
draft: false
tags:
---

# Beispiel Notiz

## Wie sollten Notizen aussehen?

<!-- Dieser Abschnitt wird noch gefüllt -->

---

## Syntax-Beispiele

### Callouts (Obsidian)

> [!note] Note
> Für allgemeine Hinweise.

> [!tip] Tip
> Für hilfreiche Tipps.

> [!warning] Warning
> Für Warnungen.

> [!danger] Danger
> Für kritische Hinweise.

> [!example] Example
> Für Beispiele.

> [!quote] Quote
> Für Zitate.

> [!info]- Einklappbar (standardmäßig eingeklappt)
> Dieser Inhalt ist einklappbar.

> [!tip]+ Einklappbar (standardmäßig ausgeklappt)
> Dieser Inhalt ist auch einklappbar.

### Wikilinks (Obsidian)

- Einfacher Link: [[index]]
- Link mit Anzeigetext: [[index|Zurück zur Startseite]]
- Link zu Überschrift: [[index#Mitwirken]]
- Externer Link: [Quartz Dokumentation](https://quartz.jzhao.xyz)

### Tabellen (GFM)

| Spalte 1 | Spalte 2 | Spalte 3 |
|----------|:--------:|---------:|
| Links    | Zentriert| Rechts   |
| Text     | Text     | Text     |

### Tasklisten (GFM)

- [ ] Unerledigte Aufgabe
- [x] Erledigte Aufgabe
- [ ] Noch eine Aufgabe

### Durchgestrichen (GFM)

~~Dieser Text ist durchgestrichen.~~

### Fußnoten (GFM)

Hier ist ein Satz mit einer Fußnote.[^1]

Und noch einer mit einer benannten Fußnote.[^note]

[^1]: Das ist die erste Fußnote.
[^note]: Fußnoten können auch benannt werden.

### Code

Inline: `code`

Block mit Syntax-Highlighting:

```python
def hello():
    print("Hello, Hive Mind!")
```

### Mathematik (LaTeX)

**Inline:** Der Satz des Pythagoras ist $a^2 + b^2 = c^2$ und Einsteins Formel $E = mc^2$.

**Block:**

$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$

**Brüche und Wurzeln:**

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

**Summen und Produkte:**

$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2} \qquad \prod_{i=1}^{n} i = n!
$$

**Matrizen:**

$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
\cdot
\begin{pmatrix}
x \\
y
\end{pmatrix}
=
\begin{pmatrix}
ax + by \\
cx + dy
\end{pmatrix}
$$

**Griechische Buchstaben:** $\alpha, \beta, \gamma, \delta, \epsilon, \theta, \lambda, \pi, \sigma, \omega$

**Weitere Symbole:** $\infty, \partial, \nabla, \forall, \exists, \in, \notin, \subset, \cup, \cap$

### Bilder und Embeds

Bild: `![Alt Text](pfad/zum/bild.png)`

Obsidian Embed: `![[andere-notiz]]`

PDF Embed: `![[dokument.pdf]]`
