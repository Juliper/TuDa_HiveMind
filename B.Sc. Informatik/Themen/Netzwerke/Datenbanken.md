---
title: Datenbanken
description: Grundlagen der Datenbankensysteme
tags:
  - netzwerke
---

# Datenbanken

Datenbanken speichern und verwalten strukturierte Daten effizient.

## Relationales Modell

Daten werden in Tabellen (Relationen) organisiert:

| ID | Name | Alter |
|----|------|-------|
| 1 | Anna | 22 |
| 2 | Bob | 25 |

### Schlüssel

| Typ | Beschreibung |
|-----|--------------|
| Primärschlüssel | Eindeutige Identifikation |
| Fremdschlüssel | Verweis auf andere Tabelle |

## SQL

### Grundoperationen

```sql
-- Abfrage
SELECT name, alter FROM studenten WHERE alter > 21;

-- Einfügen
INSERT INTO studenten (name, alter) VALUES ('Carl', 23);

-- Aktualisieren
UPDATE studenten SET alter = 26 WHERE name = 'Bob';

-- Löschen
DELETE FROM studenten WHERE id = 1;
```

### Joins

```sql
SELECT s.name, v.titel
FROM studenten s
JOIN einschreibungen e ON s.id = e.student_id
JOIN vorlesungen v ON e.vorlesung_id = v.id;
```

## ACID-Eigenschaften

| Eigenschaft | Bedeutung |
|-------------|-----------|
| Atomicity | Ganz oder gar nicht |
| Consistency | Konsistenter Zustand |
| Isolation | Transaktionen unabhängig |
| Durability | Änderungen dauerhaft |

## NoSQL

| Typ | Beispiel | Anwendung |
|-----|----------|-----------|
| Document | MongoDB | Flexible Schemas |
| Key-Value | Redis | Caching |
| Graph | Neo4j | Beziehungen |

## Siehe auch

- [[Authentifizierung|Authentifizierung]]

---

> [!abstract] Relevant für
> Informationsmanagement, SE
