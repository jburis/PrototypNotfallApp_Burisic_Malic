# README: Apple Watch Notfall-App Prototyp (V2.0)

## Projektübersicht

Dieses Dokument fasst die Konzeption und die iterative Entwicklung eines interaktiven Prototypen für eine Apple Watch App zusammen, die für Ärzte im Notfalleinsatz entwickelt wurde. Das primäre Ziel ist es, kritische Patienteninformationen (Vitalwerte, Allergien, EKG) auf einen Blick und mit minimaler Interaktion zugänglich zu machen.

Der Prototyp wurde als interaktive HTML/CSS/JS-Websimulation erstellt, um den Swipe-Flow und das WatchOS-Design direkt im Browser testbar zu machen.

### Erstellungshinweis

Die gesamte Analyse des Mockups, die Notfall-Optimierung und die Erstellung des interaktiven Codes wurden von **Gemini** (dem von Google entwickelten Modell) durchgeführt.

## 1. Ausgangssituation (Analyse der Skizze)

Basierend auf dem hochgeladenen PDF-Mockup (`Status des Patienten.pdf`) wurde die App zunächst in eine 3-seitige Struktur (mit Swipe-Geste) unterteilt:

| Seite | Inhalt | Anmerkung |
| :--- | :--- | :--- |
| **Seite 1** | Status (Herzfrequenz, Rhythmus, SpO2, Blutdruck) | Direkter Überblick. |
| **Seite 2** | Kontext (Bewegungsprofile, Medikamente, Allergien) | Hintergrundinformationen. |
| **Seite 3** | Analyse (Chronische Erkrankungen, EKG) | Tiefergehende medizinische Details. |

**Gestellte Fragen und Klärungen:**
* Die ursprüngliche Annahme, das EKG sei auf Seite 1, wurde korrigiert: Das EKG befindet sich auf **Seite 3** mit den Chronischen Erkrankungen.
* Die Notwendigkeit einer **Vergrößerung der Schriftgröße** wurde als entscheidend für die Notfallsituation erkannt.

## 2. Iteration auf Version 2.0 (Notfalloptimierung)

Die Version 2.0 (Aktueller Code) wurde entwickelt, um die App für den Notfall-Einsatz zu optimieren. Die Struktur und das Design wurden neu gewichtet, um nach dem Prinzip der **Informationshierarchie** zu arbeiten.

### Neue Features und Anpassungen (V2.0)

| Feature | Beschreibung | Grund/Empfehlung |
| :--- | :--- | :--- |
| **Größere Textgrößen** | Deutliche Vergrößerung aller kritischen Zahlen (28px Schriftgröße) und Labels für maximale Lesbarkeit unter Stress. | Direkte Nutzeranforderung und essenziell für Notfall-UX. |
| **Alarm-Farbgebung** | Demonstration eines kritischen Zustands (z.B. SpO2 auf 90%) durch Hervorhebung in leuchtendem Rot (--critical-color). | Signalisiert sofort Handlungsbedarf (Circulation/Breathing-Priorität). |
| **Allergie-Priorität** | Die Information Allergien wurde von Seite 2 auf **Seite 1** verschoben und in einem rot umrandeten Feld hervorgehoben. | Allergien sind im Notfall lebensrettende Triage-Informationen (können Therapieentscheidungen sofort ändern). |
| **Quick-Action Button** | Ein großer, roter Button **"NOTFALLPROTOKOLL STARTEN"** wurde auf Seite 1 hinzugefügt. | Startet eine vordefinierte Kette von Aktionen: Team-Alarmierung, Start des Zeitstempels für die Reanimationsdokumentation, Aktivierung von Checklisten. |
| **Medikamenten-Highlight** | Auf Seite 2 werden kritische Medikamente (z.B. Betablocker) visuell hervorgehoben. | Liefert schnellen Kontext zu potenziellen Wirkungen im Notfall. |
| **EKG-Analyse-Label** | Auf Seite 3 wird der Rhythmus (z.B. "Sinusrhythmus") in großer Schrift über der Kurve angezeigt. | Schnelle visuelle Bestätigung der maschinellen Rhythmus-Analyse. |
