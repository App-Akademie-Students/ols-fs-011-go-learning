# Go Curriculum

  
## 1. Grundlagen
- Programmaufbau: `package`, `import`, `main`
- Variablen, Konstanten, Grundtypen und Typumwandlungen
- Operatoren, Ausgaben mit `fmt` und kurze Deklaration `:=`
- Bedingungen (`if`, `switch`) und Schleifen (`for`)
- Funktionen, Parameter, Rückgabewerte und Gültigkeitsbereiche


## 2. Collections
- Arrays und Slices: Index, `len`, `append`, Teilbereiche
- `range` für Schleifen über Collections und Strings
- Maps: anlegen, lesen, ändern, löschen und Existenz prüfen
- Strings und UTF-8-Grundlagen


## 3. Datenmodellierung
- Structs und zusammengesetzte Daten
- Methoden und Pointer: Werte ändern und unnötiges Kopieren vermeiden
- Interfaces: Verhalten beschreiben und Typen entkoppeln
- Eigene Packages und Sichtbarkeit von Namen

  
## 4. Fehlerbehandlung
- Mehrere Rückgabewerte und das `error`-Interface
- Fehler prüfen und weitergeben (`if err != nil`)
- Fehler mit Kontext ergänzen; Fehler nicht ignorieren
- `defer` für aufräumende Aktionen

  
## 5. Spätere Themen
- Tests mit `testing` und tabellengesteuerte Tests
- Generics für wiederverwendbare Funktionen und Typen
- Nebenläufigkeit: Goroutines, Channels und `select`
- Context, Abbruch und einfache Synchronisierung
- Module, externe Pakete und kleine vollständige Programme

## Lernreihenfolge
- Grundlagen → Collections → Structs und Methoden → Interfaces und Packages
- Fehlerbehandlung nach Funktionen; anschließend Fehler in Packages und Tests
- Tests vor größeren Programmen; Generics und Nebenläufigkeit zuletzt