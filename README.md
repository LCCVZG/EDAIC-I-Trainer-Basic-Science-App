# EDAIC Gesetze-Quiz

Installierbare Web-App (PWA) mit **246 Übungsfragen** im EDAIC-Part-I-Format (Multiple True/False: Stamm + 5 Aussagen)
zu physiologischen und physikalischen Gesetzen, Messtechnik, Kurveninterpretation und Epidemiologie/Statistik –
jede Aussage mit Erklärung, jede Frage mit Kernaussage und Merkspruch.

Fachliche Grundlage: Morgan & Mikhail's Clinical Anesthesiology, Deranged Physiology, *Physics for Anaesthetists* (FRCA).
Alle Fragen sind eigene Formulierungen und wurden in zwei Review-Durchläufen fachlich gegengeprüft.

## Veröffentlichen über GitHub Pages

1. Neues Repository auf GitHub anlegen (z. B. `edaic-gesetze-quiz`), **öffentlich**.
2. Alle Dateien dieses Ordners hochladen (Drag & Drop auf der Repository-Seite → *Add file → Upload files*), inklusive
   `.nojekyll` und dem Ordner `icons/`.
3. *Settings → Pages → Build and deployment*: **Source: Deploy from a branch**, Branch **main**, Ordner **/ (root)** → Save.
4. Nach etwa einer Minute ist die App unter `https://<benutzername>.github.io/edaic-gesetze-quiz/` erreichbar.

Auf dem Handy: Seite öffnen → im Browsermenü **„Zum Startbildschirm hinzufügen“** (iOS Safari) bzw. **„App installieren“** (Android Chrome).
Danach läuft die App auch offline.

## Aktualisieren

Geänderte Dateien einfach erneut hochladen (überschreiben). Die Datei `sw.js` enthält eine Versionsnummer (Inhalts-Hash);
mit jeder neuen Version laden installierte Apps beim nächsten Öffnen automatisch die neuen Dateien und bieten
„jetzt aktualisieren“ an. Die Dateien werden mit `build_pwa.py` aus `template.html` und `all_questions.json` erzeugt
(im Quell-Projekt, nicht im Repository nötig).

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | die App (Oberfläche und Logik) |
| `questions.js` | alle Fragen als JavaScript-Datenobjekt |
| `manifest.webmanifest` | PWA-Manifest (Name, Icons, Standalone-Modus) |
| `sw.js` | Service Worker für Offline-Betrieb und Updates |
| `icons/` | App-Icons |
| `.nojekyll` | verhindert die Jekyll-Verarbeitung auf GitHub Pages |

## Fortschritt

Der Lernfortschritt wird lokal im Browser bzw. in der installierten App gespeichert. Über **Fortschritt exportieren / Importieren**
in der Seitenleiste lässt er sich als JSON-Datei auf ein anderes Gerät übertragen; beim Import werden beide Stände
zusammengeführt (pro Frage gewinnt die neuere Antwort).

## Fragen bearbeiten

Jede Frage in `questions.js` hat die Felder `id`, `topic`, `law`, `stem`, `items` (5 × `text`, `answer`, `explanation`),
`keypoint`, `mnemonic`, `source` und optional `figure` (SVG) / `figcaption`. Nach Änderungen an `questions.js`
die Version in `sw.js` (Zeile `const CACHE = ...`) und in `index.html` (`questions.js?v=...`) anpassen, damit installierte Apps die Änderung laden.

Version: `c0850016`
