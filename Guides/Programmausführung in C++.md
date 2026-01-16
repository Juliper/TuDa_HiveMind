---
aliases:
draft: false
tags:
  - guide
---

### Preprocessing

Der Präprozessor arbeitet rein textuell, ohne Kenntnis von C++-Syntax oder Typen.
Hierfür kann man im Code Directives verwenden; hier ein paar relevante Beispiele:
- **#include** bewirkt, dass der Inhalt der inkludierten Datei 1:1 an diese Stelle kopiert wird!
- Es gibt einige conditional directives. Zum Beispiel **#ifdef**:
```cpp
#ifdef TABLE_SIZE
int table[TABLE_SIZE];
#endif
```
Die Deklaration von *table* wird hier nur kompiliert, wenn die Konstante TABLE_SIZE existiert.
- **#define**:
```cpp
#define TABLE_SIZE 100
int table1[TABLE_SIZE];
int table2[TABLE_SIZE];
```
Hier wird schlicht und ergreifend überall TABLE_SIZE durch 100 ersetzt (ohne dass der Präprozessor C++ wirklich versteht)

Eine einzelne .cpp-Quelldatei inclusive der Inhalte aller direkt oder indirect inkludierten Headerdateien wird auch **Translation Unit** genannt.
### Kompilierung

Beim Kompilieren werden Syntax und Typen geprüft und Maschinencode generiert.
Aus jeder .cpp-Datei entsteht hierbei eine Objektdatei (.o / .obj), eine Symboltabelle (welche Funktionen/Variablen definiert oder benötigt werden) und unaufgelöste Referenzen.

Jede .cpp-Datei wird **unabhängig** kompiliert!
Insbesondere kennt der Kompiler also nicht die Implementierungen anderer .cpp-Dateien.
Folgendes kleine Beispielskript kompiliert also problemlos, obwohl foo() noch nirgendwo implementiert wurde; erst beim *Linken* wird evtl. festgestellt, dass keine Implementierung existiert.
```cpp
// foo.h
void foo();

// main.cpp
#include "foo.h"
int main() {
    foo();
}
```

### Linken

Der Linker nimmt alle Objektdateien und Bibliotheken und verbindet die beim Kompilieren erarbeiteten Referenzen mit Definitionen über Dateien hinweg.

Ein beliebtes Tool fürs Linken, das auch im Praktikum verwendet wird, ist [[CMake]].


### One Definition Rule

- Im gesamten Programm darf es für jede Nicht-inline-Funktion und jede Nicht-inline-Variable nur eine Definition geben. (Bei inline-Objekten darf es mehrere identische Definition geben.) Fürs Linken mit [[CMake]] bedeutet das konkret, dass in einem Executable oder einer Library nicht mehrere Definitionen vorkommen dürfen.
- In jeder (einzelnen) Translation Unit dürfen Typen, Funktionen, Objekte und Templates nur eine Definition haben.
- **Hinweis:** Über die Anzahl an Deklarationen macht die ODR keine Aussage.

--> Deshalb ist es insbesondere wichtig, dass man
1. in einer .cpp-Datei nie andere .cpp-Dateien inkludiert und 
2. in einer Headerdatei nicht leichtfertig Sachen definiert, sondern i.A. nur deklariert

Beispiel für 1.:
```cpp
// math_utils.cpp
int add(int a, int b) {
    return a + b;
}

// main.cpp
#include "math_utils.cpp"
```
Hier wird beim Linken ein Fehler geworfen, da nach dem Preprocessing in zwei Translation Units (math_utils.cpp und main.cpp) eine (identische) Definition von *add* existiert.

Beispiel für 2.:
```cpp
// header.h
int x = 42;   // Definition!

// a.cpp
#include "header.h"
...

// b.cpp
#include "header.h"
...
```
Hier wird beim Linken ein Fehler geworfen, da nach dem Preprocessing in zwei Translations Units (a.cpp und b.cpp) eine (identische) Definition von x existiert.