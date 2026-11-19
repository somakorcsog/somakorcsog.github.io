# Economics with Soma Korcsog

Blog und Portfolio für meine Economics-Aufgaben. Reines HTML, CSS und JavaScript, kein Build-Schritt.

## Vorschau starten

- **Windows:** Doppelklick auf `start-preview.bat` (braucht Python). Der Browser öffnet http://localhost:8000.
- **Mac:** Doppelklick auf `start-preview.command`.

`index.html` direkt per Doppelklick zu öffnen funktioniert nicht, weil der Browser dann `posts.json` nicht laden darf.

## Interview-Video einfügen

1. Video als MP4 exportieren.
2. Datei umbenennen in `wu-interview.mp4`.
3. In den Ordner `media/` legen.
4. Seite neu laden. Der Platzhalter wird automatisch durch das Video ersetzt.

Tipp: GitHub erlaubt Dateien bis 100 MB. Bei einem größeren Video lade es auf YouTube hoch (auch „nicht gelistet“ geht) und gib mir den Link.

## Neue Aufgabe hinzufügen

Alle Beiträge stehen in `posts.json`. Einfach Claude schreiben: „Add this as a new assignment“ und Text, Videos, Audio oder Präsentationen mitschicken.

Unterstützte Bausteine (`blocks`):

| type | Felder | Wofür |
|---|---|---|
| `text` | `content` | Text mit **fett**, _kursiv_, Listen, ### Überschriften |
| `heading` | `text` | Große Abschnittsüberschrift |
| `notes` | `label`, `content` | Hervorgehobener Notizkasten |
| `video` | `src`, `title`, `caption`, `poster`, `portrait` | MP4-Datei aus `media/` (`portrait: true` für Hochformat) |
| `youtube` | `url`, `caption` | YouTube-Link |
| `audio` | `src`, `title`, `caption` | MP3 / Podcast |
| `pdf` | `src`, `title` | PDF eingebettet |
| `slides` | `url`, `title` | Google Slides oder Canva |
| `image` | `src`, `caption` | Bild |
| `gallery` | `images` (Liste mit `src`, `caption`) | Bildergalerie mit Vergrößern |
| `quiz` | `title`, `questions` (`q`, `options`, `answer`, `explain`) | Interaktives Quiz |
| `quote` | `content`, `author` | Zitat |
| `reflection` | `content`, optional `label` | Kasten „What I learned“ mit Somas eigener Meinung (nur echte Sätze von Soma, nie erfinden) |
| `link` | `url`, `text` | Button mit Link |

Kategorien: Introduction, Markets, Money, Business Cycles, Sustainability, Europe, International, Excursions & Events.

Weitere Felder pro Beitrag: `cover` (Titelbild) oder `coverArt` (`big`, `small`, `tone`: navy, graphite, sand, green, red, sky). Begriffe für das Glossar stehen unter `glossary`.

## Regeln bei jeder neuen Aufgabe (für Claude)

1. **Quiz erweitern:** Für jedes neue Assignment 2 bis 3 neue Fragen in `challenge.questions` in `posts.json` ergänzen (`q`, 4 `options`, `answer`, `explain`, `post` = id des Assignments). Nicht zu schwer, nicht babyleicht.
2. **What I learned:** Soma nach 2 bis 3 eigenen Sätzen fragen und als Block `reflection` am Ende des Beitrags einfügen (vor dem Quiz-Block). Soma schreibt Deutsch, auf Englisch übersetzen.
3. **Key terms:** Neue Fachbegriffe in `glossary` ergänzen (`term`, `definition`, `post`).
4. **How it was made:** Somas Wunsch auf Englisch in `makingOf.prompts` eintragen.
5. Nach CSS/JS-Änderungen die Version `?v=` in `index.html` erhöhen.
