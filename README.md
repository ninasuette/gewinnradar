# GewinnRadar – Mini-PWA

Eine einfache lokale Gewinnspiel-Verwaltung für Instagram-Screenshots.

## Start

Die Dateien auf einen statischen HTTPS-Webhost laden (z. B. GitHub Pages oder Netlify). Danach die URL in Safari auf dem iPhone öffnen und über Teilen → Zum Home-Bildschirm hinzufügen installieren.

Für einen lokalen Test: `python3 -m http.server 8000` und `http://localhost:8000` öffnen.

## Funktionen
- Screenshot importieren und OCR mit Tesseract.js (Deutsch/Englisch) durchführen
- Profil, Auslosungsdatum, Uhrzeit und Benachrichtigungsart heuristisch erkennen
- Angaben vor dem Speichern korrigieren
- Nach Datum, Status und Methode filtern; Erledigt/Entfolgen markieren
- Daten lokal speichern; JSON-Sicherung exportieren/importieren

## Grenzen
- OCR lädt beim ersten Aufruf Bibliothek und Sprachmodelle über das Internet. Die Bilder werden im Browser verarbeitet.
- Screenshot-Texte sind oft unvollständig; es gibt keine Garantie für korrekt erkannte Termine. Besonders Teilnahmeschluss vs. Auslosung prüfen.
- Screenshots werden nicht dauerhaft gespeichert, nur erkannter Text und Einträge.
- Keine automatische Instagram-Anmeldung, kein Folgen/Entfolgen, keine Push-Benachrichtigungen.
- Browserdaten löschen kann Einträge entfernen. Regelmäßig JSON-Sicherung exportieren.
- Datumsangaben ohne Jahr sind unsicher und sollten überprüft werden.
