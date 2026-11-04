# Go lernen

Dieses Projekt begleitet den Einstieg in Go mit kurzen, aufeinander aufbauenden Übungen und einem KI-Tutor. Behandelt werden unter anderem Variablen, Bedingungen, Schleifen, Funktionen und Slices.

Der KI-Tutor richtet Erklärungen und Übungen am Lernstand aus. Er prüft zunächst das Vorwissen, gibt Aufgaben zum selbstständigen Lösen und unterstützt bei Bedarf mit schrittweisen Hinweisen, Feedback und passenden Folgeübungen.

Die Tutor-Dateien liegen in `ai-tutor/`:

- `learning-rules.md` beschreibt die Didaktik und den Ablauf der Tutor-Sessions.
- `curriculum.md` legt Themen und Lernreihenfolge fest.
- `learner-state.md` hält bearbeitete Lernziele und den bekannten Lernstand fest.

Die Datei `.agents/skills/go-tutor/SKILL.md` bindet diese Vorgaben als Go-Tutor-Skill für die Sessions ein.

## Go installieren

Lade Go über den [offiziellen Download](https://go.dev/dl/) herunter und installiere die passende Version für dein Betriebssystem. Details findest du in der [Installationsanleitung](https://go.dev/doc/install).

Starte danach das Terminal und gegebenenfalls VS Code neu. Prüfe die Installation mit:

```sh
go version
```

### Alternative: Nix und direnv

Mit [Nix](https://nixos.org/) (Flakes aktiviert) und [direnv](https://direnv.net/) stellt das Projekt Go, `gopls`, `goimports` und `delve` selbst bereit. Erlaube die Umgebung einmalig im Projektordner:

```sh
direnv allow
```

Ohne direnv startest du die Umgebung mit `nix develop`.

## VS Code einrichten

1. Installiere [Visual Studio Code](https://code.visualstudio.com/).
2. Öffne die Erweiterungen (`Strg+Umschalt+X`, macOS: `Cmd+Umschalt+X`) und installiere [Go](https://marketplace.visualstudio.com/items?itemName=golang.go) von **Go Team at Google**.
3. Öffne eine `.go`-Datei und bestätige die angebotene Installation zusätzlicher Go-Werkzeuge wie `gopls`.

Die Erweiterung unterstützt Codevervollständigung, Formatierung, Tests und Debugging.

## Optional: Cloud

Für die Entwicklung mit Google Cloud kannst du [Cloud Code](https://docs.cloud.google.com/code/docs/vscode/install) ergänzen. Für lokale Go-Projekte ist keine Cloud-Erweiterung nötig.
