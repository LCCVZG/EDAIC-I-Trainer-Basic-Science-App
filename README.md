# EDAIC Gesetze-Quiz

Installierbare Web-App (PWA) für das **EDAIC Part I (Paper A)**: 571 Aufgaben – Multiple-True/False-Fragen (Stamm + 5 Aussagen),
acht Fallserien mit je fünf aufeinander aufbauenden Fragen und 25 Zeichenaufgaben, bei denen man Kurven selbst zeichnet und beschriftet, sowie 40 Rechenaufgaben mit Zahleneingabe und vollständigem Lösungsweg.
Jede Aussage mit Erklärung, jede Frage mit Kernaussage und Merkspruch. Dazu Übungsrunden (frei zusammenstellbar, Prüfungssimulation),
Pomodoro-Timer, Statistik und Offline-Betrieb.

Fachliche Grundlage: Morgan & Mikhail's Clinical Anesthesiology, Deranged Physiology, Cross/Plunkett *Physics, Pharmacology and Physiology for Anaesthetists*,
Middleton *Physics in Anaesthesia*, Marino *The ICU Book*. Alle Fragen sind eigene Formulierungen und wurden unabhängig fachlich gegengeprüft.

| Thema | Aufgaben |
|---|---|
| Herz-Kreislauf | 60 |
| Atmung & Gasaustausch | 60 |
| Niere, Wasser & Säure-Basen | 45 |
| Neurophysiologie & Temperatur | 40 |
| Pharmakokinetik & Inhalationsanästhetika | 50 |
| Physik: Gase, Flüssigkeiten & Wärme | 60 |
| Messtechnik, Monitoring & Elektrizität | 60 |
| Kurven & Graphen | 46 |
| Epidemiologie & Statistik | 20 |
| Blut, Leber & Endokrinium | 25 |
| Fallserien | 40 |
| Graphen zeichnen | 25 |
| Rechnungen | 40 |

## Veröffentlichen über GitHub Pages
1. Öffentliches Repository anlegen (z. B. `edaic-gesetze-quiz`).
2. Alle Dateien dieses Ordners hochladen (*Add file → Upload files*), inklusive `.nojekyll` und `icons/`. Beim Aktualisieren die alten Dateien einfach überschreiben.
3. *Settings → Pages*: **Deploy from a branch**, Branch **main**, Ordner **/ (root)**.
4. Nach etwa einer Minute unter `https://<benutzername>.github.io/edaic-gesetze-quiz/` erreichbar. Auf dem Handy „Zum Home-Bildschirm“ bzw. „App installieren“.

Installierte Apps erkennen neue Versionen automatisch (Versions-Hash in `sw.js`) und bieten „jetzt aktualisieren“ an.

## Fortschritt
Lokal im Browser bzw. in der App. **Exportieren/Importieren** in der Seitenleiste überträgt Antworten und Rundenverlauf auf ein anderes Gerät (Zusammenführung: pro Frage gewinnt die neuere Antwort).

Version: `e368d687`
