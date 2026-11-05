# Go-Curriculum

Die Reihenfolge unten ist der empfohlene Lernweg. Ziele dürfen nach den Lernregeln übersprungen oder wiederholt werden. IDs verbinden Curriculum, Lernstand und Lernskript.

| ID | Lernziel | Voraussetzungen | Zielkompetenz |
|---|---|---|---|
| G1 | Programmaufbau: `package`, `import`, `main`; `fmt.Println` | keine | Kleines Programm schreiben und Ablauf erklären |
| G2 | Variablen, `:=`, `=`, Konstanten, Grundtypen, Typumwandlungen | G1 | Werte passend deklarieren, ändern und umwandeln |
| G3 | Operatoren, ganzzahlige Division, `%`, Ausgaben | G2 | Ausdrücke anwenden und Ergebnisse begründen |
| G4 | Bedingungen mit `if`, `switch`; Schleifen mit `for` | G2, G3 | Entscheidungen und Wiederholungen implementieren |
| G5 | Funktionen, Parameter, mehrere Rückgabewerte, Gültigkeitsbereiche | G4 | Kleine Funktionen selbstständig entwerfen |
| F1 | Fehler als Werte, `error`, `if err != nil`, Weitergabe, `defer` | G5; `error` als gezielt eingeführtes Interface | Fehlerpfade behandeln und Ressourcen aufräumen |
| C1 | Arrays, Slices, Index, `len`, `append`, Teilbereiche, `range` | G4, G5 | Collections verarbeiten |
| C2 | Maps: anlegen, lesen, ändern, löschen, Existenz prüfen | C1 | Daten mit Schlüsseln verwalten |
| C3 | Strings, UTF-8, Bytes, Runen, `range` | C1 | Bytezugriff und Unicode-Verarbeitung unterscheiden |
| D1 | Structs und zusammengesetzte Daten | G5, C1 | Eigene Datenstrukturen modellieren |
| D2 | Pointer, Methoden, Value- und Pointer-Receiver | D1 | Änderungen und Kopieren nachvollziehen |
| D3 | Interfaces, implizite Erfüllung, Interface-Werte | D2 | Verhalten entkoppeln und Methodensignaturen prüfen |
| P1 | Eigene Packages, Sichtbarkeit, Module, externe Pakete | G5, F1; Übungsmodul zuvor bei Bedarf bereitstellen | Code aufteilen und Abhängigkeiten verwalten |
| F2 | Fehler mit Kontext ergänzen und in Packages weitergeben | F1, D3, P1 | Fehlerketten sinnvoll behandeln |
| T1 | Tests mit `testing`, tabellengesteuerte Tests | F2 | Verhalten und Fehlerfälle testen |
| A1 | Kleines vollständiges Programm | C2, C3, D3, T1 | Bisherige Konzepte zusammenführen |
| S1 | Generics für Funktionen und Typen | D3, T1 | Wiederverwendung sinnvoll abwägen |
| S2 | Goroutines, Channels, `select` | A1 | Einfache Nebenläufigkeit erklären und einsetzen |
| S3 | Context, Abbruch, Synchronisierung | S2 | Nebenläufige Arbeit begrenzen und koordinieren |

Für jedes Ziel erfolgt die Bestätigung durch eine selbstständige Aufgabe und einen leicht veränderten Transfer gemäß `learning-rules.md`. Bei Bedarf Ziele in kleinere Konzepte aufteilen.

## Hintergrund und Quellen

Historische Einflüsse bei passenden Themen kurz und sachlich einordnen:

- C-Familie: grundlegende Syntax.
- Pascal-/Modula-/Oberon-Familie: Deklarationen und Packages.
- CSP-geprägte Sprachen wie Newsqueak und Limbo: Nebenläufigkeit.

Quelle: [Offizielle Go-FAQ: Vorläufer](https://go.dev/doc/faq#ancestors). Java, C++ und Python werden in den [Entwurfsprinzipien](https://go.dev/doc/faq#principles) als Kontext diskutiert. Ein didaktischer Vergleich belegt für sich keinen historischen Einfluss.
