# Go lernen

Dieses Projekt begleitet den Einstieg in Go mit kurzen, aufeinander aufbauenden Übungen und einem KI-Tutor. Behandelt werden unter anderem Variablen, Bedingungen, Schleifen, Funktionen und Slices.

Der KI-Tutor richtet Erklärungen und Übungen am Lernstand aus. Er prüft zunächst das Vorwissen, gibt Aufgaben zum selbstständigen Lösen und unterstützt bei Bedarf mit schrittweisen Hinweisen, Feedback und passenden Folgeübungen.

## Dateien und ihre Bedeutung

Die Übersicht beschreibt die vorhandenen Projektdateien einschließlich der versteckten Konfigurationsdateien. Prompt-Sammlungen sind ausgenommen.

| Datei | Bedeutung | Bearbeitung|
|---|---|---|
| [README.md](README.md) | Einstieg in das Projekt: Dateiaufbau, Installation, Einrichtung und Anleitung zum Zurücksetzen. | Ja – Anleitung bei Bedarf aktualisieren. |
| [AGENTS.md](AGENTS.md) | Einstieg für den KI-Agenten: legt fest, wann der Go-Tutor-Skill zu lesen ist, und verweist auf Lernregeln und Sitzungszustand. Unterscheidet Lernen von Wartungsarbeiten. | Bei Bedarf – Agentenvorgaben anpassen. |
| [.agents/skills/go-tutor/SKILL.md](.agents/skills/go-tutor/SKILL.md) | Beschreibt den Tutor-Ablauf von Diagnose und eigenem Versuch über Feedback und Folgeübungen bis zur Dokumentation. Verweist für konkrete Regeln auf die Tutor-Dateien. | Bei Bedarf – Tutor-Ablauf anpassen. |
| [ai-tutor/learning-rules.md](ai-tutor/learning-rules.md) | Zentrale Regeln für Didaktik, Hilfestufen, Kompetenzbewertung, Codeprüfung und Dokumentation. Definiert die native Aktionsauswahl mit Fertig, Pausieren, Abbrechen und Überspringen sowie die zugehörigen Sitzungsübergänge. | Bei Bedarf – Lernregeln anpassen. |
| [ai-tutor/curriculum.md](ai-tutor/curriculum.md) | Lernziele mit IDs, Voraussetzungen, Zielkompetenzen und empfohlener Reihenfolge. Enthält Quellen zu historischen Einflüssen auf Go. | Ja – Lernziele und Reihenfolge anpassen. |
| [ai-tutor/learner-profile.md](ai-tutor/learner-profile.md) | Persönliche Angaben zu Vorkenntnissen, Lernzielen, Vorlieben und Bezugssprachen. Enthält nur ausdrücklich genannte Angaben; unbekannte Angaben bleiben als solche markiert. | Ja – eigene Angaben ergänzen oder korrigieren; auch vom Tutor gepflegt. |
| [ai-tutor/learner-state.md](ai-tutor/learner-state.md) | Langfristiger Lernstand: trennt Bearbeitungsstatus, belegte Kompetenz, Hilfen und offene Nachweise. Hält auch übersprungene Ziele und Wiederholungsbedarf fest. | Normalerweise vom Tutor gepflegt; Korrekturen oder bewusster Reset möglich. |
| [ai-tutor/session-state.md](ai-tutor/session-state.md) | Kurzfristiger Aufgabenstand mit Vorgangs-ID, Erfolgskriterien, Dateipfad, Hilfen, Status, Historie und nächstem Schritt. Ermöglicht Pause und Wiederaufnahme und bewahrt frühere Vorgänge. Ein Aufgabenstatus allein ist kein Kompetenznachweis. | Normalerweise vom Tutor gepflegt; Korrekturen oder bewusster Reset möglich. |
| [ai-tutor/learning-script.md](ai-tutor/learning-script.md) | Persönliches Lernskript mit Erklärungen, Beispielen, geklärten Fehlvorstellungen und Wiederholungsfragen. Wächst mit bestätigtem Fortschritt; vorläufige Inhalte sind gekennzeichnet. | Normalerweise vom Tutor gepflegt; eigene Notizen und Korrekturen möglich. |
| [ai-tutor/interaction-test.md](ai-tutor/interaction-test.md) | Protokoll des Tests der nativen Fertig-Bestätigung: verfügbare Tools, Ablauf, Ergebnis und Grenzen der Prüfung. Dient der technischen Dokumentation und ist selbst kein Lernnachweis. | Bei Bedarf – Testergebnisse aktualisieren. |
| [go.mod](go.mod) | Definiert das Go-Modul `go-learning` für das Projekt und die darunterliegenden Übungspakete. Kann später Go-Version und Modulabhängigkeiten aufnehmen. | Bei Bedarf – Modulkonfiguration anpassen; auch durch Go-Werkzeuge gepflegt. |
| [main.go](main.go) | Einfaches Startprogramm in der Projektwurzel mit einer Begrüßung. Wird mit `go run .` aus der Projektwurzel ausgeführt. | Ja – Programm selbst bearbeiten. |
| [.gitignore](.gitignore) | Legt fest, welche erzeugten Dateien und lokalen Einstellungen Git normalerweise ignoriert, etwa Programme, Build- und Testausgaben sowie lokale Workspace- und VS-Code-Dateien. | Bei Bedarf – Ausschlussregeln anpassen. |
| [exercises/01-variablen/main.go](exercises/01-variablen/main.go) | Übungsprogramm zur Deklaration und Neuzuweisung einer Variablen mit anschließender Ausgabe. | Ja – eigene Übungslösung bearbeiten. |
| [exercises/02-programmaufbau/main.go](exercises/02-programmaufbau/main.go) | Schreibübung zu Package, Import, Programmeinstieg und zwei aufeinanderfolgenden Ausgaben mit `fmt.Println`. | Ja – eigene Übungslösung bearbeiten. |
| [exercises/03-programmaufbau-transfer/main.go](exercises/03-programmaufbau-transfer/main.go) | Eigenständige Folgeübung zum Programmaufbau: Import und Einstieg ergänzen und mit genau einem `fmt.Println`-Aufruf die geforderte Zeile ausgeben. Aufgabenstatus und Prüfung stehen im Sitzungszustand. | Ja – eigene Übungslösung bearbeiten. |

Jeder nummerierte Ordner unter `exercises/` enthält einen eigenen Versuch. Führe `go run .` im jeweiligen Übungsordner aus, um genau dieses Programm zu starten. Neue Aufgaben erhalten weitere freie Ordner; bestehende Lösungen bleiben erhalten.

## Übungen wiederholen und Lernen zurücksetzen

Für einen vollständigen Neustart sollten die bisherigen Übungsordner unter `exercises/` gelöscht werden, zum Beispiel `01-variablen`, `02-programmaufbau` und `03-programmaufbau-transfer`. Sie enthalten deine bisherigen Lösungen und können neue Versuche vorwegnehmen. Der Ordner `exercises/` selbst kann bestehen bleiben; der Tutor legt neue Übungsordner an. Sichere Lösungen, die du behalten möchtest, vorher außerhalb des Übungsordners.

Nur die Übungsdateien zu löschen setzt den Tutor noch nicht zurück. Für einen vollständigen Lernreset müssen auch die persönlichen Aufzeichnungen in `ai-tutor/` zurückgesetzt werden. Behalte die folgenden Dateien als leere Grundstruktur mit eindeutigen Anfangsangaben erhalten:

| Datei | Für einen vollständigen Reset entfernen bzw. zurücksetzen |
|---|---|
| `learner-state.md` | Bisherige Beobachtungen, Kompetenzbewertungen, Nachweise, Themenwechsel und Wiederholungsplanung entfernen. Alle Curriculumziele als offen und ungeprüft kennzeichnen; kein aktuelles Lernziel vorgeben. |
| `session-state.md` | Aktuellen Vorgang, erhaltene Vorgänge und Übergangshistorien entfernen. Explizit festhalten: „Keine laufende Aufgabe; bewusster Lernreset.“ Die leere Vorlage kann bleiben. |
| `learning-script.md` | Persönlich erarbeitete Erklärungen, Beispiele und Wiederholungsfragen entfernen. Titel und Hinweis auf ein noch leeres Lernskript können bleiben. |
| `learner-profile.md` | Bei einem vollständigen persönlichen Neustart Angaben zu Vorkenntnissen, Zielen und Vorlieben auf „Unbekannt“ setzen. Beim erneuten Lernen mit demselben Profil dürfen diese Angaben erhalten bleiben. |

Optionale Aufzeichnungen wie `ai-tutor/interaction-test.md` können gelöscht werden. Prüfe auch eigene Notizen oder Sicherungskopien auf alte Lernstände.

Erhalte die Tutor-Grundlagen: `AGENTS.md`, `.agents/skills/go-tutor/SKILL.md`, `ai-tutor/learning-rules.md`, `ai-tutor/curriculum.md` sowie `go.mod` und gegebenenfalls `go.sum`. Lösche nicht pauschal den gesamten Ordner `ai-tutor/`. Ein Wiederherstellen aus Git ist nur dann ein Reset, wenn die gewählte Version tatsächlich einen leeren Lernstand enthält.

Beginne nach dem Reset einen neuen Chat, damit alte Aufgaben und Antworten aus dem bisherigen Gespräch nicht erneut als Lernstand übernommen werden. Teile dem Tutor mit: „Ich habe die Übungen und Lernaufzeichnungen bewusst zurückgesetzt. Starte das Lernen neu und diagnostiziere mein Vorwissen.“

Für die Wiederholung einer einzelnen Übung ist kein vollständiger Reset nötig: Bitte den Tutor um einen neuen Versuch in einem freien Übungsordner. Bisherige Nachweise dürfen dabei bestehen bleiben. Wenn du stattdessen den alten Übungsordner löschst, teile dies dem Tutor mit, damit er die Dateiverweise im Sitzungszustand anpasst.

## Go installieren

Lade Go über den [offiziellen Download](https://go.dev/dl/) herunter und installiere die passende Version für dein Betriebssystem. Details findest du in der [Installationsanleitung](https://go.dev/doc/install).

Starte danach das Terminal und gegebenenfalls VS Code neu. Prüfe die Installation mit:

```sh
go version
```

## VS Code einrichten

1. Installiere [Visual Studio Code](https://code.visualstudio.com/).
2. Öffne die Erweiterungen (`Strg+Umschalt+X`, macOS: `Cmd+Umschalt+X`) und installiere [Go](https://marketplace.visualstudio.com/items?itemName=golang.go) von **Go Team at Google**.
3. Öffne eine `.go`-Datei und bestätige die angebotene Installation zusätzlicher Go-Werkzeuge wie `gopls`.

Die Erweiterung unterstützt Codevervollständigung, Formatierung, Tests und Debugging.

## Optional: Cloud

Für die Entwicklung mit Google Cloud kannst du [Cloud Code](https://docs.cloud.google.com/code/docs/vscode/install) ergänzen. Für lokale Go-Projekte ist keine Cloud-Erweiterung nötig.
