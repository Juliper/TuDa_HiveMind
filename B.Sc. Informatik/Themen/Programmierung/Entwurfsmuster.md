---
title: Entwurfsmuster
description: Bewährte Lösungsschablonen für wiederkehrende Probleme
tags:
  - programmierung
---

# Entwurfsmuster

Entwurfsmuster (Design Patterns) sind bewährte Lösungsschablonen für häufig auftretende Probleme in der Softwareentwicklung.

## Kategorien

### Erzeugungsmuster
Wie Objekte erstellt werden.

| Muster | Zweck |
|--------|-------|
| Singleton | Genau eine Instanz einer Klasse |
| Factory | Objekterzeugung auslagern |
| Builder | Komplexe Objekte schrittweise aufbauen |

### Strukturmuster
Wie Klassen zusammengesetzt werden.

| Muster | Zweck |
|--------|-------|
| Adapter | Inkompatible Schnittstellen verbinden |
| Decorator | Funktionalität dynamisch erweitern |
| Composite | Baumstrukturen behandeln |

### Verhaltensmuster
Wie Objekte interagieren.

| Muster | Zweck |
|--------|-------|
| Observer | Bei Änderungen benachrichtigen |
| Strategy | Algorithmen austauschbar machen |
| Iterator | Sequentieller Zugriff auf Elemente |

## Beispiel: Singleton

```java
public class Database {
    private static Database instance;

    private Database() {}

    public static Database getInstance() {
        if (instance == null) {
            instance = new Database();
        }
        return instance;
    }
}
```

## Siehe auch

- [[Objektorientierung|Objektorientierung]]

---

> [!abstract] Relevant für
> Software Engineering, FOP
