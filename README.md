# Sociology Quest

**Sociology Quest** ist eine eigenständige deutschsprachige Lernapp für zentrale soziologische Autor*innen und Theorien. Das Repository ist als statische Website aufgebaut und kann direkt über GitHub Pages veröffentlicht werden.

## Enthalten

- 85 Theorie- und Autor\*inneneinträge in acht Modulen
- durchsuchbare Enzyklopädie mit Kerngedanken, Fachbegriffen und Literaturhinweisen
- digitale Karteikarten
- Multiple-Choice- und Lückentext-Aufgaben
- XP, Level, Serienbonus und Konfetti
- Dark Mode und Light Mode
- responsive Darstellung für Desktop, Tablet und Smartphone
- lokales Speichern des Lernfortschritts im Browser
- keine externen Abhängigkeiten, kein Tracking, kein Build-Schritt

## Lokal starten

Die App besteht vollständig aus `index.html`. Für einen schnellen Test kann die Datei direkt per Doppelklick geöffnet werden.

Zuverlässiger ist ein kleiner lokaler Webserver:

```bash
python -m http.server 8000
```

Danach im Browser `http://localhost:8000` öffnen.

## Auf GitHub hochladen

1. Auf GitHub ein neues, leeres Repository anlegen, zum Beispiel `sociology-quest`.
2. Alle Dateien aus diesem Ordner in das Repository hochladen. `index.html` muss im obersten Verzeichnis liegen.
3. Änderungen auf den Standard-Branch `main` übertragen.

Alternativ mit Git:

```bash
git init
git add .
git commit -m "Sociology Quest veröffentlichen"
git branch -M main
git remote add origin https://github.com/DEIN-NAME/sociology-quest.git
git push -u origin main
```

## GitHub Pages aktivieren

1. Im GitHub-Repository **Settings** öffnen.
2. Links **Pages** auswählen.
3. Unter **Build and deployment** bei **Source** die Option **Deploy from a branch** wählen.
4. Als Branch **main** und als Ordner **/(root)** auswählen.
5. **Save** anklicken.

Nach kurzer Zeit zeigt GitHub dort die öffentliche Adresse an. Sie hat üblicherweise dieses Format:

`https://DEIN-NAME.github.io/sociology-quest/`

Für diese App ist keine GitHub Action und kein Build-Workflow erforderlich.

## Daten und Datenschutz

Der Lernfortschritt wird über `localStorage` ausschließlich im jeweils verwendeten Browser gespeichert. Es werden keine Daten an einen Server übertragen. Wird der Browser-Speicher gelöscht oder ein anderes Gerät verwendet, steht der dortige Lernstand nicht zur Verfügung.

## Inhalte bearbeiten

Alle Inhalte, Gestaltung und Funktionen befinden sich in `index.html`. Die Theoriedaten stehen im JavaScript-Abschnitt in der Liste `rawTheories`. Jeder Eintrag enthält:

1. Modul-ID
2. Theorietitel
3. Autor\*in
4. Lebensdaten
5. Kerngedanke
6. Fachbegriffe, getrennt durch `|`
7. kanonischen Literaturhinweis

Die Erläuterungen dienen dem systematischen Lernen und ersetzen nicht die Lektüre der Primärtexte. Begriffe, Übersetzungen und Datierungen können je nach Ausgabe variieren.

## Lizenz

Der Programmcode steht unter der MIT-Lizenz. Siehe [LICENSE](LICENSE).
