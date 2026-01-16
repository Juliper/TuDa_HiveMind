---
title: CMake
aliases:
draft: false
tags:
  - guide
---


**1.**     **Zweck von CMake und grundlegende Begriffe**

CMake dient dazu, in C++ automatisiert Build-Dateien zu generieren, die von Build-Systemen wie Make verwendet werden können. Dazu werden sogenannte **Targets** verwendet. Targets lassen sich unterteilen in **Libraries** (= Bibliotheken, bei uns z.B. _relearn_lib_, _relearn_gpu_ und _range-v3_) und **Executables** (bei uns z.B. _relearn_, _relearn_tests_ und _relearn_benchmarks_). Jedes Target wird mit mehreren Quelldateien assoziiert. Executables lassen sich nach dem Kompilieren ausführen (wer hätte es gedacht, Details siehe unten). Libraries lassen sich nicht ausführen. Sie können aber mittels _target_link_libraries_ (siehe unten) mit Executables oder anderen Libraries verknüpft werden, damit diese anderen Targets auf die Quelldateien in der Library zugreifen können.


**2.**     **Einige relevante CMake-Befehle:**

**add_executable(my_executable main.cpp other_source.cpp)**: erstellt ein Executable namens _my_executable_ und fügt diesem _main.cpp_ und _other_source.cpp_ als Quelldateien hinzu. Bei Ausführung des Executables wird die Datei ausgeführt, in der die _main_-Methode definiert ist (traditionell ist das die erstgenannte Datei, hier also _main.cpp_)

**add_library(my_library STATIC source1.cpp source2.cpp)**: erstellt eine Library namens _my_library_ und fügt dieser _source1.cpp_ und _source2.cpp_ als Quelldateien hinzu. Es gibt statische und dynamische Libraries: Statische Libraries werden zur Compilezeit direkt in ausführbare Programme, die sie brauchen, eingebunden. Dynamische Libraries (-> **SHARED** statt **STATIC**) werden erst zur Laufzeit geladen und müssen dadurch auch nur einmal im Speicher geladen werden.

**target_sources(my_target PRIVATE source1.cpp source2.cpp)**: fügt dem (bereits bestehenden) Target _my_target_ (kann Executable oder Library sein) die Quelldateien _source1.cpp_ und _source2.cpp_ hinzu.

**target_link_libraries(my_executable PRIVATE my_library)**: Verknüpft die Library _my_library_ mit dem Executable _my_executable_, d.h. _my_executable_ kann auf alle Quelldateien aus _my_library_ zugreifen. Man kann auch zwei Libraries miteinander verknüpfen und "transitiv" längere Verknüpfungsketten erzeugen.

**target_include_directories(my_target PUBLIC dir):** bewirkt, dass alle Dateien, die mit _my_target_ assoziiert sind, als zusätzlichen Startpunkt für relative Suchpfade _dir_ wählen


**3.**     **Konkretes Beispiel:** 

**Aufgabe:** Wie kann ich beim Linken mit CMake sicherstellen, dass ich in einer Datei namens e.cc auf eine Methode m in einer Datei d.cc (im gleichen Projekt) zugreifen kann?

Merksatz (laut ChatGPT): **Alles, was beim Linken gebraucht wird, muss Teil desselben Targets sein oder explizit gelinkt werden.**

Minimallösung:
```cpp
add_executable(program e.cc d.cc)
```

strukturierte Lösung für reale Projekte:
```cpp
add_library(d_lib d.cc d.h)
add_executable(programm e.cc)
target_link_libraries(programm PRIVATE d_lib)
```

Die strukturierte Lösung hat z.B. folgende Vorteile:
- **schnelleres Kompilieren bei Änderungen**: Bei Änderungen muss CMake nur d_lib neu kompilieren.
- **bessere Wiederverwendbarkeit:** Andere Executables können einfach d_lib wiederverwenden; bei der Minimallösung hingegen müsste man d.cc jedes mal explizit mit in add_executable() aufnehmen
- **sauberere Trennung:** Bibliotheken sollten die Implementierung einer Funktionalität sein; Executables sollten "Anwendungen" sein, die die Bibliothek nutzen
