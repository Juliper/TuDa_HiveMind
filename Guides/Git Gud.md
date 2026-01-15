---
title: Git Gud
aliases:
draft: false
tags:
  - guide
---


### Basics 

Das **Arbeitsverzeichnis** ist der Ordner, in dem das Gitprojekt auf dem eigenen Computer gespeichert ist. Es beinhaltet die Dateien des aktuell ausgecheckten Branches sowie einen versteckten Unterordner .git mit allen Metadaten (siehe Abschnitt 2). Der Inhalt dieses Unterordners ist das **lokale Repository**. Das **Remote-Repository** ist die Version deines Projekts, die auf einem anderen Server (z.B. GitHub) gespeichert ist und mit dem lokalen Repository synchronisiert werden kann mittels Remote-Tracking-Branches (siehe ebenfalls Abschnitt 2). _Analogie:_ Arbeitsverzeichnis ≙ Schreibtisch, Branch ≙ Ordner, den man aus dem Archiv (≙ dem lokalen Repository) holt und auf den Schreibtisch legt zum Arbeiten 
### Einige wichtige Komponenten des lokalen Repos
- _config_: Konfigurationsdatei, die z.B. Benutzername/Email, Remote-URLs für die Branches, u.v.m. enthält
- _refs/remotes/_: enthält Referenzen für die **Remote-Tracking-Branches**. Das sind Abbilder der **Remote-Branches** auf Github, die mit _git fetch_ aktualisiert werden.
- _refs/heads/_: enthält Referenzen für die **lokalen Branches**. Diese müssen explizit mit dem zugehörigen Remote-Tracking-Branch synchronisiert werden mit _git merge_. (_git push_ ist einfach eine Kombination aus _git fetch_ und _git merge_.)
- _objects/_: die eigentliche Datenbank mit den tatsächlichen Daten der Commits, Dateien ...
- _index:_ speichert den **Staging-Bereich** oder **Index**, wo Änderungen im Arbeitsbereich mit git add hinzugefügt werden müssen, bevor sie mit _git commit_ ins Repo übernommen werden können
### Ein paar spezielle Gitbefehle
    
- *git add --all,  git commit -a -m "Kommentar",  git push*:  grundlegende Schritte, um Code in Remote-Repository hochzuladen
- *git fetch --prune*: lädt alle Inhalte des Remote-Repo ins lokale Repo. _--prune_ bewirkt, dass Branches gelöscht werden, die es im Remote nicht mehr gibt.
- _git checkout -b xyz origin/xyz:_ Erstellt einen neuen lokalen Branch namens xyz basierend auf dem Remote-Tracking-Branch origin/xyz
- _git branch -a:_ zeigt alle Branches an, inklusive der Remotebranches
- *git restore . :* setzt alle geänderten Dateien auf den letzten Commit zurück

### Weiterführendes

Hier eine nützliche URL für "Probleme" mit Git: https://ohshitgit.com/de
    