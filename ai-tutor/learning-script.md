# Persönliches Go-Lernskript

Dieses Skript wächst mit bestätigtem Lernfortschritt. Maßgeblich für Kompetenz und offene Ziele bleibt `learner-state.md`. Bestehende Abschnitte werden überarbeitet; Lösungen offener Übungen werden nicht vorweggenommen.

## G1: Programmaufbau und Ausgabe

Programmaufbau und zwei Ausgabezeilen wurden am 2026-11-04 in `exercises/02-programmaufbau/main.go` erfolgreich geprüft. In `exercises/03-programmaufbau-transfer/main.go` ergänzte die lernende Person anschließend selbstständig den Import, Programmeinstieg und einen `fmt.Println`-Aufruf; `go run .` gab exakt die geforderte Zeile aus. Im Transfer sagte sie zwei Aufrufe mit `fmt.Println` als zwei Zeilen voraus und begründete, weshalb der Import nötig ist. G1 ist damit abgeschlossen.

Ein ausführbares Go-Programm verwendet `package main`. Seine Funktion `main` ist der Programmeinstieg. Imports machen benötigte Packages verfügbar.

`import "fmt"` macht das Package unter dem Namen `fmt` verfügbar; `fmt.Println(...)` ruft dessen Funktion `Println` auf. Ein unbenutzter Import wird vom Compiler abgelehnt. Werden alle Verwendungen von `fmt` entfernt, muss auch dieser Import entfernt werden. Die Importrolle wurde zunächst nach Erklärung geklärt und anschließend im selbstständigen Transfer bestätigt.

```go
package main

import "fmt"

func main() {
    fmt.Println("Hallo Go")
}
```

`fmt.Println` beendet jede Ausgabe mit einer neuen Zeile. Bei mehreren Argumenten trennt es die Werte durch Leerzeichen.

Wiederholungsfrage: Welche Aufgabe haben `package main`, `import` und `func main()` jeweils?

## G2: Deklaration, Zuweisung und Konstanten

Die Unterscheidung wurde im bisherigen Lernstand beobachtet; selbstständige Anwendung und Transfer noch offen.

```go
punkte := 2
punkte = 3
const maximum = 10
```

`:=` deklariert hier eine lokale Variable und bestimmt ihren Typ aus dem Anfangswert. `=` weist einer bestehenden Variablen einen Wert zu. Eine Konstante kann nicht neu zugewiesen werden.

Wiederholungsfrage: Woran erkennst du im Beispiel die Deklaration und die spätere Änderung?

### Vorläufig: Grundtypen und Typumwandlung

`int` wird für untypisierte ganzzahlige Konstanten als Standardtyp verwendet, `float64` für untypisierte Gleitkommakonstanten bei entsprechender Typableitung. Im bisherigen Lernstand war bei `float64` eine Korrektur nötig; selbstständige Bestätigung fehlt.

Eine nicht-ganzzahlige untyped float constant wie `int(6.2)` ist unzulässig, weil ihr Wert nicht exakt als `int` darstellbar ist. Bei `y := 6.2` erhält `y` den Standardtyp `float64`; eine explizite Umwandlung `int(y)` ist zulässig und schneidet den Nachkommaanteil gegen null ab. Die lernende Person hat diesen Unterschied und das Ergebnis `6` selbstständig auf ein neues Beispiel übertragen.

Quelle: [Go-Spezifikation: Konvertierungen](https://go.dev/ref/spec#Conversions).

## G3: Operatoren

Bisher beobachtet; Selbstständigkeit und Transfer noch zu prüfen.

Bei ganzzahligen Operanden liefert `/` ganzzahlige Division; `%` liefert den Divisionsrest. Multiplikation bindet stärker als Addition. Klammern machen eine gewünschte Auswertungsreihenfolge deutlich.

Wiederholungsfrage: Wie unterscheiden sich ganzzahlige Division und Division mit Gleitkommazahlen?

## Weitere Abschnitte

D3 bleibt aktuelles Übungsziel. Ergänze dazu erst nach bestätigtem Fortschritt einen Abschnitt, ohne offene Übungsantworten vorwegzunehmen. Sprachvergleiche folgen, sobald Bezugssprachen im Nutzerprofil bekannt sind.
