# 🎮 BEREICH 03: GAME DEVELOPMENT
**Archiv:** PROMTS | **Letztes Update:** April 2026  
**Zugehöriger Skill:** `game-forge-2d`

---

## [GAME-01] 2D HTML5 SPIEL — VOLLSTÄNDIGER AUFBAU

**Wann:** Ein neues Browser-basiertes 2D-Spiel von Grund auf erstellen.  
**Usage-Note:** Multi-File-Architektur, keine monolithischen Einzeldateien.

```
Erstelle ein vollständiges 2D HTML5/JavaScript Spiel.

KONZEPT:
- Name: [NAME]
- Genre: [GENRE: Platformer / RPG / Puzzle / Arcade / Card Game / etc.]
- Core Loop: [WAS MACHT DER SPIELER IN EINEM ZYKLUS]
- Zielplattform: Browser (Desktop + Mobile)
- Multiplayer: [JA → Socket.io Node.js / NEIN → Single Player]

GAMEPLAY:
- Steuerung: [TASTATUR / TOUCH / MAUS]
- Progression: [LEVEL / SCORE / UNLOCKS / CARDS]
- Win/Lose-Bedingung: [BESCHREIBEN]

TECHNISCHER STACK:
- Multiplayer: Node.js + Socket.io + HTML5 Canvas
- Single Player: HTML5 Canvas + Vanilla JS oder Phaser.js
- Hosting wenn Multiplayer: Render.com (kostenlos, Auto-Deploy via GitHub)

ARCHITEKTUR (Multi-File):
- index.html — Entry Point
- src/game/GameState.js — Spielzustand
- src/game/[Domain].js — Weitere Module
- public/css/style.css — Styling

NACH FERTIGSTELLUNG:
1. 10 Code-Iterations-Prüfungen
2. Multi-Agenten-Review
3. GitHub Push: https://github.com/phunkhazardcrew-svg/[REPO]
4. Deployment-Anleitung für Render.com
```

---

## [GAME-02] DIGIMON WORLD: REBORN — FEATURE ENTWICKLUNG

**Wann:** Arbeiten am Digimon World PS1 Remake (Python/Pygame).  
**Usage-Note:** Immer erst Checkpoint von Drive laden, dann erst coden.

```
Wir arbeiten am Digimon World: Reborn Projekt.

LADE ZUERST: Aktuellen Projektstand aus Google Drive und GitHub:
- Repo: https://github.com/phunkhazardcrew-svg/Digimon-World-1-Rebuild-2D
- Drive-Checkpoint: [CHECKPOINT-ID]

AUFGABE DIESE SESSION: [BESCHREIBEN]

PROJEKT-RAHMENBEDINGUNGEN:
Engine: Python 3.x + Pygame
Datenmodell: JSON-Datenbanken
  - digimon.json: Alle Digimon-Definitionen (Stages, Stats, Types)
  - attacks.json: 55+ Techniken (7 Elemente: Feuer, Eis, Donner, Wind, Erde, Licht, Dunkel)
  - evolutions.json: Digitations-Pfade mit Stat-Requirements + Pflege-Faktoren
  - areas.json: 16 File Island Gebiete

STORY-TREUE: File Island Struktur, File City, Analogman als Antagonist
STYLE: 2D Tile-basierte Top-Down-Darstellung (NICHT 1:1 PS1-Texturen)
ROSTER: Original 65 Digimon + Erweiterungen erlaubt

DIGITATIONS-SYSTEM:
- Triggered durch: Kampf-Stats, Pflege-Fehler-Anzahl, Schlaf-Pattern
- Kein direkter Level-Up — Körpergewicht, Trainings-Counts, Care-Mistakes zählen

NACH SESSION-ENDE:
1. Checkpoint-Datei erstellen
2. Progress auf Google Drive sichern
3. Auf GitHub pushen mit semantischem Commit
```

---

## [GAME-03] MULTIPLAYER BACKEND — NODE.JS + SOCKET.IO

**Wann:** Online-Multiplayer-Funktionalität aufbauen oder erweitern.

```
Entwickle/Erweitere das Multiplayer-Backend.

SPIEL: [NAME]
AUFGABE: [NEUE FEATURE / BUGFIX / REFACTOR]

TECHNISCHER STACK:
- Backend: Node.js + Express + Socket.io
- Frontend: HTML5 Canvas + Vanilla JS
- Hosting: Render.com (Free Tier, GitHub Auto-Deploy)

SOCKET EVENTS die implementiert werden müssen:
- Client→Server: [LISTE DER EVENTS]
- Server→Client: [LISTE DER EVENTS]

SPIELZUSTAND:
- Was wird serverseitig gehalten? [BESCHREIBEN]
- Was ist clientseitig? [BESCHREIBEN]
- Wie wird Cheating verhindert? [SERVER-AUTHORITY]

EDGE CASES:
- Spieler disconnected mitten im Spiel
- Host-Migration wenn Ersteller disconnected
- Reconnect innerhalb von [X] Sekunden erlaubt

NACH FERTIGSTELLUNG:
- 10 Iterations-Prüfung
- Multi-Agenten-Review
- Push auf GitHub
- Deploy auf Render.com überprüfen
```

---

## [GAME-04] GAME DESIGN DOCUMENT (GDD)

**Wann:** Für neue Spielprojekte oder um bestehende zu dokumentieren.

```
Erstelle ein Game Design Document für:

SPIEL-NAME: [NAME]
PLATTFORM: [PC / Browser / Mobile]
GENRE: [GENRE]

GDD-STRUKTUR:
1. Executive Summary (1 Seite)
2. Vision & Zielgruppe
3. Core Game Loop (Flussdiagramm)
4. Spielmechaniken im Detail
5. Progression-System
6. Content-Plan (Level, Items, Charaktere)
7. Technische Architektur
8. Art-Direction (Stil, Farben, Referenzen)
9. Audio-Konzept
10. Scope & Milestones

Format: Markdown, klar strukturiert, für Entwickler verständlich.
Lade anschließend auf Google Drive hoch.
```

---

## [GAME-05] SPIEL-DEBUGGING — LOGIK & REGELWERK

**Wann:** Ein Spielmechanismus verhält sich nicht wie erwartet.

```
Das Spiel [NAME] hat folgenden Regelwerk-Fehler:

PROBLEM: [BESCHREIBEN — z.B. "Kampf wird nicht ausgelöst wenn Monster im selben Raum"]
ERWARTETES VERHALTEN: [WAS SOLLTE PASSIEREN]
TATSÄCHLICHES VERHALTEN: [WAS PASSIERT STATTDESSEN]
REGELWERK-QUELLE: [ORIGINAL-REGEL aus Rulebook / GDD]

ANALYSE-ANFORDERUNGEN:
1. Finde die relevanten Code-Stellen (GameState, Event-Handler, Phase-Manager)
2. Trace den Fehler von Trigger bis Symptom
3. Erkläre warum der Fehler auftritt
4. Implementiere den Fix mit Regelwerk-Kommentar
5. Schreibe einen Unit-Test der den Fix verifiziert
6. Prüfe ob ähnliche Regelwerk-Verletzungen an anderen Stellen existieren
```

---

*Bereich 03 | Game Development | Stand April 2026*
