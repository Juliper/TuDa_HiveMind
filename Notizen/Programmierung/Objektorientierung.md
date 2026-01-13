---
title: Objektorientierung
description: Grundprinzipien der objektorientierten Programmierung
tags:
  - programmierung
---

# Objektorientierung

Objektorientierte Programmierung (OOP) organisiert Code um Objekte herum, die Daten und Verhalten kapseln.

## Grundprinzipien

### Kapselung
Daten und Methoden werden in Objekten gebündelt. Zugriff wird über Sichtbarkeiten gesteuert.

```java
public class Konto {
    private double kontostand;  // gekapselt

    public void einzahlen(double betrag) {
        this.kontostand += betrag;
    }
}
```

### Vererbung
Klassen können Eigenschaften und Methoden von anderen Klassen erben.

```java
public class Girokonto extends Konto {
    private double dispoLimit;
}
```

### Polymorphismus
Objekte verschiedener Klassen können über eine gemeinsame Schnittstelle angesprochen werden.

```java
Konto konto = new Girokonto();  // Polymorphismus
konto.einzahlen(100);
```

### Abstraktion
Komplexität wird durch abstrakte Klassen und Interfaces versteckt.

## Siehe auch

- [[Entwurfsmuster|Entwurfsmuster]]
- [[Rekursion|Rekursion]]

---

> [!abstract] Relevant für
> FOP, Software Engineering, AuD
