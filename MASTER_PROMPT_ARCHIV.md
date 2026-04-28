# 📚 MASTER PROMPT ARCHIV — Dominik
**Version:** 1.0 | **Erstellt:** April 2026 | **Sprache:** Deutsch  
**Zweck:** Zentrales Prompt-Template-Repository für alle Arbeitsbereiche  
**GitHub:** https://github.com/phunkhazardcrew-svg  
**Push Token:** [TOKEN_REDACTED]

---

## 📋 INHALTSVERZEICHNIS

| # | Bereich | Datei |
|---|---------|-------|
| 0 | **Universal-Prompts** (immer anwendbar) | `00_UNIVERSAL.md` |
| 1 | **Manufacturing Tools** (Python/tkinter) | `01_MANUFACTURING_TOOLS.md` |
| 2 | **CNC & CAM** (HyperMILL, TNC7, Tebis) | `02_CNC_CAM.md` |
| 3 | **Game Development** (Digimon, 2D Games) | `03_GAME_DEV.md` |
| 4 | **Austin Relocation & Admin** | `04_AUSTIN_ADMIN.md` |
| 5 | **Kreativprojekte & Schreiben** (What If?) | `05_KREATIV_SCHREIBEN.md` |
| 6 | **Finanzen & Verkauf** | `06_FINANZEN_VERKAUF.md` |
| 7 | **Gesundheit & Ernährung** | `07_GESUNDHEIT.md` |
| 8 | **KI-Workflow & Technik** | `08_KI_WORKFLOW.md` |
| 9 | **GitHub & Versionskontrolle** | `09_GITHUB.md` |

---

## ⚙️ WIE MAN DIESES ARCHIV BENUTZT

### Option A — Direktkopie
Prompt aus der gewünschten Bereichsdatei kopieren → anpassen → einfügen.

### Option B — Claude instruieren
> „Verwende den Prompt [NAME] aus dem PROMTS-Archiv für folgende Aufgabe: [BESCHREIBUNG]"

### Option C — Batch-Modus
Mehrere Prompts kombinieren:
> „Verwende Universal-Prompt UNI-03 (Code-Iteration) kombiniert mit Manufacturing-Prompt MFG-01 für dieses Tool."

---

## 🔑 SECTION 0: UNIVERSAL-PROMPTS

*Diese Prompts gelten für JEDE Anfrage und werden immer auf das jeweilige Thema angewendet.*

---

### [UNI-01] RÜCKFRAGEN-PROMPT
**Wann:** Vor jeder ausführlichen Antwort, besonders bei komplexen Anfragen.  
**Zweck:** Sicherstellt dass Claude den richtigen Kontext hat.

```
Bevor du mit der Umsetzung beginnst:
1. Fasse kurz zusammen was du verstanden hast was ich von dir verlange.
2. Stelle maximal 3 gezielte Rückfragen die für eine hochwertige Umsetzung essenziell sind.
3. Warte auf meine Antwort bevor du loslegst.

Fange NICHT mit der Umsetzung an bevor ich deine Zusammenfassung und Fragen abgesegnet habe.
```

---

### [UNI-02] MULTI-AGENTEN-REVIEW-PROMPT
**Wann:** Nach jeder wichtigen Ausgabe (Code, Dokument, Plan).  
**Zweck:** Qualitätskontrolle durch mehrere Review-Perspektiven.

```
Führe jetzt ein Multi-Agenten-Review durch:

AGENT 1 — QUALITÄTSPRÜFER:
Prüfe die Ausgabe auf: Vollständigkeit, Korrektheit, fehlende Elemente.

AGENT 2 — KRITIKER:
Was ist schwach, unklar, oder könnte besser sein? Mindestens 3 Punkte.

AGENT 3 — DEVIL'S ADVOCATE:
Was könnte schief gehen? Welche Annahmen wurden gemacht die falsch sein könnten?

AGENT 4 — OPTIMIERER:
Wie kann die Ausgabe in Version 2 verbessert werden?

Fasse alle Review-Ergebnisse zusammen und erstelle eine verbesserte Version 2.
```

---

### [UNI-03] CODE-ITERATIONS-PROMPT (mindestens 10 Durchläufe)
**Wann:** Bei jeder Code-Erstellung oder -Überarbeitung.  
**Zweck:** Systematische Fehlerbereinigung vor der finalen Ausgabe.

```
Analysiere den folgenden Code in MINDESTENS 10 Iterationen:

ITERATION 1: Überschusscode — Gibt es überflüssigen Code der entfernt werden kann?
ITERATION 2: Syntaxfehler — Offensichtliche Syntaxfehler und Tippfehler
ITERATION 3: Logikfehler — Fehler in der Programmlogik (falsche Bedingungen, Endlosschleifen etc.)
ITERATION 4: Fehlende Imports / Abhängigkeiten — Werden alle nötigen Module importiert?
ITERATION 5: Namenskonflikte — Doppeldeutige Variablennamen, shadowing, scope-Probleme
ITERATION 6: Edge Cases — Was passiert bei leeren Eingaben, None-Werten, falschen Datentypen?
ITERATION 7: Error Handling — Sind alle relevanten Fehlerquellen abgefangen?
ITERATION 8: Performance — Offensichtliche Performance-Probleme (unnötige Schleifen, O(n²))
ITERATION 9: Security — Unsichere Operationen (Pfad-Traversal, Injection etc.)
ITERATION 10: Konsistenz — Sind Namenskonventionen, Stil und Formatierung konsistent?

Nach allen 10 Iterationen: Erstelle die saubere, korrigierte Finalversion.
```

---

### [UNI-04] CHECKPOINT-PFLICHT-PROMPT
**Wann:** Bei jeder komplexen Aufgabe mit mehreren Schritten.  
**Zweck:** Kein Kontext- und Fortschrittsverlust.

```
Für diese Aufgabe gilt:
1. Erstelle SOFORT zu Beginn eine _progress.json im Arbeitsverzeichnis
2. Aktualisiere die Datei nach JEDEM abgeschlossenen Schritt
3. Erstelle nach jedem Meilenstein eine Checkpoint-Datei (CHECKPOINT_[NAME].md)
4. Nutze Google Drive als permanente Ablage wenn verfügbar
5. Jede Checkpoint-Datei muss enthalten: Stand, erledigte Schritte, offene Schritte, nächste Aktion

Zeige am Ende jedes Schrittes das Status-Dashboard:
╔═══════════════════════════════════╗
║  TASK: [Name]                     ║
║  Fortschritt: [X/Y Schritte]      ║
║  Nächster Schritt: [Beschreibung] ║
╚═══════════════════════════════════╝
```

---

### [UNI-05] PLANUNG-VOR-UMSETZUNG-PROMPT
**Wann:** Vor jedem größeren Projekt oder komplexen Build.  
**Zweck:** Strukturierter Ansatz statt sofortigem Losbauen.

```
Bevor du anfängst:
1. Erstelle einen vollständigen Projektplan mit allen Schritten in logischer Reihenfolge
2. Schätze den Aufwand pro Schritt (klein/mittel/groß)
3. Identifiziere mögliche Risiken und Abhängigkeiten
4. Lege die Dateistruktur fest
5. Definiere das Erfolgs-Kriterium: Wann ist die Aufgabe fertig?

Präsentiere den Plan für meine Absegnung BEVOR du mit dem ersten Schritt anfängst.
```

---

### [UNI-06] GOOGLE-DRIVE-PUSH-PROMPT
**Wann:** Nach Fertigstellung jedes Deliverables.  
**Zweck:** Sicherung aller Ergebnisse in Google Drive.

```
Lade alle erstellten Dateien auf Google Drive hoch:
- Erstelle falls nicht vorhanden einen passenden Ordner mit sprechendem Namen
- Lade jede Hauptdatei als eigenes Dokument hoch
- Lade Checkpoints und Dokumentation separat hoch
- Gib mir die Drive-Links zu allen hochgeladenen Dateien
- Erstelle eine Übersicht was wo gespeichert wurde
```

---

### [UNI-07] GITHUB-PUSH-PROMPT
**Wann:** Bei Code-Projekten nach Fertigstellung oder wichtigen Meilensteinen.  
**Zweck:** Versionskontrolle und Backup auf GitHub.

```
Push alle Änderungen auf GitHub:
- Repository: [REPO-NAME] (https://github.com/phunkhazardcrew-svg/[REPO-NAME])
- Token: [TOKEN_REDACTED]
- Erstelle aussagekräftige Commit-Messages nach dem Schema: [type](scope): Beschreibung
- Setze Tags für wichtige Meilensteine
- Gib mir eine Übersicht der gepushten Commits und Tags
```

---

## 🔧 SECTION 1: MANUFACTURING TOOLS (Python/tkinter)

*Vollständige Referenz: `01_MANUFACTURING_TOOLS.md`*

### [MFG-01] TOOL-ERSTELLUNG GRUNDPROMPT
**Wann:** Immer wenn ein neues Python/tkinter Desktop-Tool für Manufacturing erstellt wird.  
**Zweck:** Setzt sofort den richtigen Standard und verhindert fehlende Grundkomponenten.

```
Erstelle ein professionelles Python/tkinter Desktop-Tool mit folgenden Pflichtanforderungen:

PFLICHT-ARCHITEKTUR (Single-File):
1. Docstring mit ASCII-Art Header, Toolname, Version, Autor
2. Phase 1: Standard-Library Imports
3. Phase 2: Pfaddefinitionen (SCRIPT_DIR, SETTINGS_FILE, LOG_FILE)
4. Phase 3: SingleInstanceLock (verhindert mehrfaches Starten)
5. Phase 4: High-DPI Aktivierung (VOR tkinter Import!)
6. Phase 5: Bootstrapper (Auto-Dependency-Installation mit pip)
7. Phase 6: Externe Imports (tkinter, dann Third-Party)
8. Hilfs-Funktionen: _lighten(), _darken() für Farbmanipulation
9. Tesla Dark Theme Konstanten:
   - BG_DARK = "#1A1A1A"
   - BG_CARD = "#242424"  
   - BG_INPUT = "#2E2E2E"
   - ACCENT = "#E31937"
   - TEXT_PRIMARY = "#FFFFFF"
   - TEXT_SECONDARY = "#AAAAAA"
   - BORDER = "#3A3A3A"
10. Settings-System (JSON-basiert, load_settings/save_settings)
11. Business-Logik-Klassen
12. Custom Widgets: TBtn (Canvas-Button mit Hover), TProgress
13. MainApp-Klasse mit _build_header(), _build_body(), _build_footer()
14. GlobalExceptionHandler (mit Crash-Log)
15. if __name__ == "__main__": Block

TOOL-BESCHREIBUNG:
[HIER BESCHREIBEN WAS DAS TOOL TUN SOLL]

Führe nach der Erstellung mindestens 10 Code-Iterations-Prüfungen durch.
```

---

### [MFG-02] TOOL-ERWEITERUNG / BUGFIX PROMPT
**Wann:** Wenn ein bestehendes Tool erweitert oder ein Bug gefixt wird.

```
Analysiere das bestehende Tool und:
1. Verstehe die aktuelle Architektur VOLLSTÄNDIG bevor du änderst
2. Mache einen minimalen, chirurgischen Eingriff — kein Umschreiben ohne Grund
3. Halte alle bestehenden Funktionen intakt
4. Prüfe auf Regressions (hat die Änderung etwas anderes kaputt gemacht?)
5. Dokumentiere die Änderung mit einem Changelog-Eintrag im Header

Zu änderndes Verhalten: [BESCHREIBUNG]
Betroffene Klassen/Methoden: [WENN BEKANNT]
```

---

## 🏭 SECTION 2: CNC & CAM

*Vollständige Referenz: `02_CNC_CAM.md`*

### [CNC-01] HYPERMILL VT MAKRO ENTWICKLUNG
**Wann:** Beim Erstellen oder Erweitern von HyperMILL Virtual Tool Makros.

```
Ich möchte ein HyperMILL VT (Virtual Tool) Makro entwickeln.

Mein Anwendungsfall:
[BESCHREIBEN WAS DAS MAKRO TUEN SOLL]

Bitte:
1. Erkläre die VT-Logik Schritt für Schritt im VT-Editor (keine direkten Code-Blöcke — Führung durch GUI)
2. Erkläre welche TOOL_SEARCH-Parameter gesetzt werden müssen
3. Zeige die Makro-Reihenfolge mit TRANSFER_TO_CYCLE
4. Erkläre Feature-Variablen und Connector-Variablen die relevant sind
5. Zeige wie man das Makro auf eine Bohrung testet

Technische Rahmenbedingungen:
- Maschine: [MASCHINENTYP]
- Controller: Heidenhain TNC7
- HyperMILL Version: [VERSION]
```

---

### [CNC-02] HYPERMILL AUTOMATION CENTER PYTHON
**Wann:** Beim Entwickeln von Python-Skripten für das HyperMILL Automation Center.

```
Entwickle ein Python-Skript für das HyperMILL Automation Center.

Aufgabe: [BESCHREIBEN]

Anforderungen:
- Gut kommentierter, anfängerfreundlicher Code
- Daten aus Excel-Arbeitsplan einlesen (Dateiname: [NAME], relevante Spalten: [SPALTEN])
- Fehlerbehandlung für fehlende/fehlerhafte Excel-Daten
- Logging aller Aktionen
- Ergebnis-Export als [PDF/Excel/CSV]

Halte dich an die HyperMILL Automation Center API-Konventionen.
Nach der Erstellung: 10 Iterations-Prüfung + Multi-Agenten-Review.
```

---

### [CNC-03] NC-CODE ANALYSE / OPTIMIERUNG
**Wann:** Beim Analysieren oder Optimieren von NC-Programmen.

```
Analysiere folgenden NC-Code für eine Heidenhain TNC7 Steuerung:

[NC-CODE HIER EINFÜGEN]

Prüfe auf:
1. Kollisionsrisiken (Werkzeug vs. Spannmittel, Werkzeug vs. Rohteil)
2. Ineffiziente Werkzeugwege (unnötige Leerfahrten, suboptimale Zustellung)
3. Fehlende Sicherheitsabstände
4. Nicht-TNC7-konforme Syntax
5. Optimierungspotenziale für Bearbeitungszeit

Bauteil-Kontext: [MATERIAL / OPERATION / SPANNLAGE]
```

---

## 🎮 SECTION 3: GAME DEVELOPMENT

*Vollständige Referenz: `03_GAME_DEV.md`*

### [GAME-01] 2D HTML5 SPIEL ENTWICKLUNG
**Wann:** Beim Erstellen von Browser-basierten 2D Spielen.

```
Erstelle ein vollständiges 2D HTML5/JavaScript Spiel.

SPIEL-KONZEPT:
[NAME, GENRE, KERNMECHANIK, ZIELPLATTFORM]

TECHNISCHE ANFORDERUNGEN:
- HTML5 Canvas oder Phaser.js/PixiJS
- Modular aufgebaut (keine monolithischen Dateien)
- Game Loop mit konstantem Timing (requestAnimationFrame)
- Mobile-kompatibel wenn möglich
- Sprite-Animation System

GAMEPLAY:
- Core Loop: [BESCHREIBEN]
- Steuerung: [TASTEN/TOUCH]
- Progression: [LEVEL/SCORE/UNLOCKS]

ARCHITEKTUR: Multi-File (index.html + separate JS-Module)
Nach Erstellung: Code-Iteration (10x) + Multi-Agenten-Review + GitHub-Push
```

---

### [GAME-02] DIGIMON WORLD PYTHON/PYGAME
**Wann:** Für alle Arbeiten am Digimon World Reborn Remake.

```
Wir arbeiten am Digimon World: Reborn Projekt (Python/Pygame Remake von Digimon World PS1 1999).

Aktueller Stand: [AUS CHECKPOINT/DRIVE LADEN]

Aufgabe für diese Session:
[BESCHREIBEN]

Rahmenbedingungen:
- Engine: Python + Pygame
- Daten: JSON-Datenbanken (digimon.json, attacks.json, evolutions.json, areas.json)
- 7 Elemente: Feuer, Eis, Donner, Wind, Erde, Licht, Dunkel
- Originalgetreue Story (File Island, File City, Analogman)
- Erweiterter Roster über die 65 Original-Digimon hinaus
- 2D Tile-basierte Top-Down-Darstellung

Nach der Session: Checkpoint erstellen + auf GitHub pushen.
Repo: https://github.com/phunkhazardcrew-svg/Digimon-World-1-Rebuild-2D
```

---

### [GAME-03] MULTIPLAYER SPIEL (Node.js + Socket.io)
**Wann:** Bei Online-Multiplayer Spielen.

```
Erstelle/Erweitere ein Online-Multiplayer Spiel.

TECH-STACK: Node.js + Socket.io + Express (Backend) + HTML5/Canvas (Frontend)
HOSTING: Render.com (kostenlos, GitHub-Auto-Deploy)

SPIELMECHANIK:
[BESCHREIBEN]

MULTIPLAYER-ANFORDERUNGEN:
- Echtzeit-Synchronisierung der Spielzustände
- Raum-/Lobby-System (mehrere parallele Spiele)
- Reconnect-Handling
- Mobile Browser kompatibel

Nach Erstellung: Code-Iteration (10x) + Multi-Agenten-Review + GitHub-Push + Deployment-Anleitung
```

---

## 🌎 SECTION 4: AUSTIN RELOCATION & ADMIN

*Vollständige Referenz: `04_AUSTIN_ADMIN.md`*

### [ADMIN-01] BEHÖRDEN-BRIEF / OFFIZIELLE KORRESPONDENZ
**Wann:** Bei offiziellen Briefen, Anträgen, oder behördlichen Schreiben.

```
Erstelle ein offizielles Schreiben für folgende Situation:

Absender: Dominik [Nachname], [Adresse Prüm]
Empfänger: [BEHÖRDE / ORGANISATION]
Betreff: [THEMA]
Rechtsgrundlage: [PARAGRAF / GESETZ falls bekannt]

Sachverhalt:
[SITUATION BESCHREIBEN]

Gewünschte Reaktion/Forderung:
[WAS SOLL ERREICHT WERDEN]

Format: Formelles Geschäftsschreiben auf Deutsch (DIN 5008)
Ton: Sachlich, bestimmt, rechtlich präzise
Frist setzen: [JA/NEIN] — wenn ja bis: [DATUM]
```

---

### [ADMIN-02] US-BÜROKRATIE / TEXAS SPEZIFISCH
**Wann:** Bei Fragen zu US-amerikanischen Behördengängen, Texas-spezifischen Regelungen.

```
Ich brauche aktuelle, praktische Informationen zu folgendem US/Texas-Behördenthema:

[THEMA: z.B. SSN-Antrag, Texas Driver's License, Social Security, Steuern etc.]

Mein Kontext:
- Neu-Einwanderer, Arbeitsvisa TN/H1B/E3 (Tesla Gigafactory Austin)
- Wohnort: Austin, TX (ZIP: [PLZ])
- Ankunft: Juli 2026

Benötigte Informationen:
1. Wo genau (Adresse, Büro, Website)
2. Was mitbringen (genaue Dokumente-Liste)
3. Typische Wartezeiten und Bearbeitungszeiten
4. Kosten
5. Häufige Fehler die Einwanderer machen (und wie vermeiden)

Bitte aktuell recherchieren (Stand 2026).
```

---

### [ADMIN-03] UMZUGS-STATUS-UPDATE
**Wann:** Um den aktuellen Stand aller offenen Umzugs-ToDos zu bekommen.

```
Erstelle mir einen aktuellen Status-Report meiner Austin-Umzugs-Vorbereitung.

Struktur:
1. ✅ Erledigte Punkte (mit Datum)
2. ⏳ In Bearbeitung (mit aktuellem Stand)
3. 🔴 Dringende offene Punkte (nach Deadline sortiert)
4. 📅 Zeitlinie der nächsten 4 Wochen
5. 💡 Meine Empfehlung: Was sollte ich als nächstes angehen?

Nutze alle verfügbaren Informationen aus unserem bisherigen Kontext.
```

---

## ✍️ SECTION 5: KREATIVPROJEKTE & SCHREIBEN

*Vollständige Referenz: `05_KREATIV_SCHREIBEN.md`*

### [KREATIV-01] WHAT IF? BUCH FORTSETZEN
**Wann:** Wenn am "What If?" Buchprojekt weitergearbeitet wird.

```
Wir setzen das What If? Buchprojekt fort.

Lade zuerst den aktuellen Checkpoint von Google Drive (ID: 18dKjRF5iTxjU-UOYRumKN2ifIifAtkRY).

Schreibe [Akt X / Kapitel Y]:

QUALITÄTSSTANDARDS:
- Ton: Warm, eloquent, rhythmisch — niemals akademisch
- Struktur: Hook → Etablierte Überzeugung → Anomalie → Spekulation → Implikationen → Offene Frage
- Länge: 1.500–2.000 Wörter pro Kapitel
- Kein "magisches Denken" — Spekulationen müssen wissenschaftlich denkbar sein
- Konkrete Bilder statt Abstraktionen
- Zielgruppe: Offen denkende Frauen 25–55

Nach jedem Kapitel: Multi-Agenten-Review → Überarbeitung → Google Drive Upload.
Drive-Ordner-ID: 13Mi10_bSXgiY33vpzlb9PX2k0QNDLYbQ
```

---

### [KREATIV-02] SPEKULATIVES SZENARIO ENTWICKELN
**Wann:** Beim Entwickeln neuer What If? Kapitel-Ideen.

```
Entwickle ein spekulatives Szenario nach dem What If? Prinzip.

THEMA/IMPULS: [BESCHREIBEN]

CONSTRAINTS:
✅ Erlaubt: Wissenschaftlich fundierte Spekulation, unbekannte Fakten, alternative Interpretationen
✅ Erlaubt: Spirituelle Anker wenn wissenschaftlich nicht widerlegbar
❌ Nicht erlaubt: Magie, übernatürliche Kräfte, rein mythologische Erzählungen
❌ Nicht erlaubt: Menschen laufen über Wasser, Levitation etc.

Prüfe das Szenario durch diese Linse:
1. Ist die Grundannahme wissenschaftlich denkbar? (Plausibilitäts-Check)
2. Was sind die größten Implikationen wenn es wahr wäre?
3. Welche bekannten Phänomene/Fakten passen dazu?
4. Welche offene Frage bleibt am Ende?
```

---

## 💰 SECTION 6: FINANZEN & VERKAUF

*Vollständige Referenz: `06_FINANZEN_VERKAUF.md`*

### [FIN-01] FAHRZEUG/GEGENSTAND VERKAUFSKALKULATION
**Wann:** Beim Vorbereiten eines Verkaufs auf eBay Kleinanzeigen oder ähnlichen Plattformen.

```
Erstelle eine professionelle Verkaufskalkulation für:

OBJEKT: [BESCHREIBEN / Fotos wenn vorhanden]
ZUSTAND: [ZUSTAND BESCHREIBEN]
KAUFPREIS DAMALS: [PREIS / UNBEKANNT]
SCHMERZGRENZE (NUR FÜR MICH): [BETRAG]

Aufgaben:
1. Internetrecherche: aktueller Neupreis und Gebrauchtmarktpreise auf Kleinanzeigen, eBay, Mobile.de etc.
2. Wertminderungsberechnung mit klaren Faktoren
3. Empfohlener Angebotspreis (Verkäufer-optimiert, mit Verhandlungspuffer)

Erstelle danach ZWEI PDFs:
A) INTERNE VERSION (für mich): Vollständige Analyse INKL. Schmerzgrenze
B) KÄUFER VERSION: Transparente Preisherleitung OHNE Schmerzgrenze — sachlich und verkaufsfördernd

Bevor du die PDFs erstellst, zeige mir die Parameter zur Abnahme.
```

---

### [FIN-02] INVESTITIONSSTRATEGIE / FINANZPLANUNG
**Wann:** Bei Fragen zu Investitionen, Steuern, oder finanzieller Planung.

```
Ich brauche finanzielle Orientierung zu folgendem Thema:

[THEMA]

Mein Kontext:
- Einkommensquelle ab Juli 2026: Tesla Austin, $40/h, ~$83.200/Jahr brutto
- Steuerliche Situation: DE→US-Umzug 2026, DBA Deutschland-USA relevant
- Bestehendes deutsches Bankkonto und Grundstück (weiterhin in DE)
- Investitionsziel: [BESCHREIBEN]

Bitte:
1. Erläutere die relevanten Optionen sachlich (kein Finanzberater-Ersatz)
2. Zeige steuerliche Implikationen auf (DE und US)
3. Empfehle konkrete nächste Schritte
4. Markiere klar was ich mit einem Steuerberater besprechen sollte
```

---

## 💪 SECTION 7: GESUNDHEIT & ERNÄHRUNG

*Vollständige Referenz: `07_GESUNDHEIT.md`*

### [HEALTH-01] KCAL TRACKER EINTRAG
**Wann:** Für tägliche Ernährungsprotokollierung.

```
Neuer Kcal-Tracker Eintrag für [DATUM]:

Gegessen/Getrunken:
[LISTE MIT MENGEN]

Bitte:
1. Berechne die Makros (kcal, Protein, KH, Fett)
2. Vergleiche mit meinem Tagesziel (2.170 kcal, 170g Protein, 215g KH, 70g Fett)
3. Gib kurzes Feedback (Muster, Tipp)

[Wenn ich "Post" sage: Erstelle die tägliche PDF und lade sie in den Google Drive Ordner kcal_track hoch]
```

---

### [HEALTH-02] WASSERFASTEN PROTOKOLL
**Wann:** Beim Start oder Monitoring eines Wasserfastens.

```
Wir starten / überwachen ein Wasserfasten-Protokoll.

FASTEN-START: [DATUM/UHRZEIT]
GEPLANTE DAUER: [TAGE]
AKTUELLER TAG: [X]

Bitte:
1. Zeige die physiologischen Phasen des Fastens mit Zeitachse
2. Gib Empfehlungen für Elektrolyte (Na, K, Mg)
3. Warnzeichen auf die ich achten sollte
4. Mentale Strategien für schwierige Momente

Zeichne den Fortschritt auf und erstelle nach Ende des Fastens einen Abschlussbericht.
```

---

## 🤖 SECTION 8: KI-WORKFLOW & TECHNIK

*Vollständige Referenz: `08_KI_WORKFLOW.md`*

### [KI-01] MULTI-KI-WORKFLOW PLANUNG
**Wann:** Wenn Claude mit anderen KI-Systemen kombiniert werden soll.

```
Plane einen optimalen KI-Workflow für folgende Aufgabe:

AUFGABE: [BESCHREIBEN]

Verfügbare KI-Systeme:
- Claude (API + Claude.ai + Claude Code)
- DeepSeek V4 (über API oder Open WebUI)
- Gemini (Pro/Flash)
- Ollama + Lokale Modelle (NiPoGi Pinova P1)

Bitte erstelle:
1. Aufgabenverteilung nach KI-Stärken
2. Datenfluss zwischen den Systemen
3. Konkrete API-Calls oder Workflows
4. Kosten-Schätzung
5. Setup-Anleitung für meinen NiPoGi Mini-PC (Windows 11)
```

---

### [KI-02] CLAUDE CODE / TERMINAL WORKFLOW
**Wann:** Bei Nutzung von Claude Code im Terminal.

```
Ich nutze Claude Code im Terminal für folgende Aufgabe:

AUFGABE: [BESCHREIBEN]
KONTEXT: [PROJEKTSTRUKTUR / RELEVANTE DATEIEN]

Bitte:
1. Optimale Claude Code Flags/Optionen für diese Aufgabe
2. Empfohlene .claude/settings.json Konfiguration
3. Auto-Approval Hooks falls relevant
4. Workflow-Empfehlung (welche Schritte interaktiv, welche automatisch)

Nutze GitHub für Checkpoints: https://github.com/phunkhazardcrew-svg/[REPO]
```

---

## 🐙 SECTION 9: GITHUB & VERSIONSKONTROLLE

*Vollständige Referenz: `09_GITHUB.md`*

### [GIT-01] REPOSITORY ANALYSE & BUGFIX
**Wann:** Beim Analysieren oder Reparieren eines GitHub-Repositories.

```
Analysiere das folgende GitHub-Repository und behebe [PROBLEM]:

Repository: https://github.com/phunkhazardcrew-svg/[REPO-NAME]
Auth-Token: [TOKEN_REDACTED]

Vorgehen:
1. Klone das Repo oder lese die relevanten Dateien über die GitHub API
2. Verstehe die aktuelle Architektur vollständig
3. Identifiziere das Problem
4. Erstelle einen Plan für den Fix
5. Implementiere den Fix
6. Teste (10 Iterations-Prüfung)
7. Committe mit aussagekräftiger Message: [type](scope): Beschreibung
8. Push auf main/master

Setze Tags für wichtige Meilensteine: [TAG-NAME]
```

---

### [GIT-02] REPO CHECKPOINT ERSTELLEN
**Wann:** Vor größeren Änderungen oder nach Meilensteinen.

```
Erstelle einen Git-Checkpoint für folgende Situation:

Repository: [REPO-URL]
Anlass: [MEILENSTEIN / SICHERUNG VOR ÄNDERUNG]
Tag-Name: [BESCHREIBENDER TAG]

Aktionen:
1. Aktuellen Stand committen (alle Änderungen)
2. Tag erstellen und pushen
3. Changelog-Eintrag im README / CHECKPOINT.md aktualisieren
4. Kurze Zusammenfassung was dieser Checkpoint enthält

Token: [TOKEN_REDACTED]
```

---

## 📝 PROMPT-KOMBINATIONEN (EMPFOHLEN)

### Kombination 1: Neues Manufacturing Tool
`[UNI-01] + [UNI-05] + [MFG-01] + [UNI-03] + [UNI-02] + [GIT-01] + [UNI-06]`

### Kombination 2: CNC Makro Entwicklung
`[UNI-01] + [CNC-01] + [UNI-03] + [UNI-02]`

### Kombination 3: Game Feature hinzufügen
`[UNI-01] + [GAME-02] + [UNI-03] + [UNI-02] + [GIT-01]`

### Kombination 4: Behördenbrief / Admin
`[ADMIN-01] + [UNI-02]`

### Kombination 5: Buchkapitel schreiben
`[KREATIV-01] + [UNI-02] + [UNI-06]`

### Kombination 6: Fahrzeug verkaufen
`[FIN-01] + [UNI-02]`

---

## 🔄 CHANGELOG

| Datum | Version | Änderung |
|-------|---------|----------|
| 2026-04-28 | 1.0 | Initial Release — 9 Bereiche, 25+ Prompts |

---

*Erstellt von Claude auf Basis der gesamten Chat-Historie mit Dominik | April 2026*
