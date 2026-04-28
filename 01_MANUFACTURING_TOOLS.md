# 🔧 BEREICH 01: MANUFACTURING TOOLS (Python/tkinter)
**Archiv:** PROMTS | **Letztes Update:** April 2026  
**Zugehöriger Skill:** `manufacturing-tool-forge`

---

## ÜBERSICHT

Alle Prompts für das Erstellen, Erweitern und Debuggen von Python/tkinter Desktop-Tools für Manufacturing-, CAD/CAM- und Büro-Workflows.

**Standard-Stack:**
- Python 3.x + tkinter
- Tesla Dark Theme (`#1A1A1A`, `#E31937`, `#FFFFFF`)
- JSON-Konfiguration
- Auto-Dependency-Installation (Bootstrapper)
- SingleInstanceLock + Crash-Handler
- PyInstaller für `.exe` Export

---

## [MFG-01] TOOL-NEUERSTELLUNG — VOLLSTÄNDIGER GRUNDPROMPT

**Wann:** Immer wenn ein neues Python/tkinter Tool von Grund auf erstellt wird.  
**Usage-Note:** Diesen Prompt IMMER verwenden — er setzt die komplette Architektur.  
**Kombinieren mit:** `[UNI-01]`, `[UNI-03]`, `[UNI-02]`, `[GIT-01]`

```
Erstelle ein professionelles Python/tkinter Desktop-Tool für Manufacturing-Automatisierung.

TOOL-NAME: [NAME]
TOOL-ZWECK: [WAS SOLL ES TUN]
EINGABEN: [WELCHE DATEIEN / INPUTS]
AUSGABEN: [WELCHE DATEIEN / OUTPUTS / AKTIONEN]

PFLICHT-ARCHITEKTUR (Single-File, in dieser Reihenfolge):

1. ASCII-Art Header mit Toolname, Version, Beschreibung, Autor
2. Phase 1: Standard-Library Imports (os, sys, json, pathlib, subprocess, logging)
3. Phase 2: Pfade
   - SCRIPT_DIR = Path(__file__).parent
   - SETTINGS_FILE = SCRIPT_DIR / "[toolname]_settings.json"
   - LOG_FILE = SCRIPT_DIR / "[toolname].log"
4. Phase 3: SingleInstanceLock (filelock-basiert)
5. Phase 4: High-DPI Aktivierung
   - Windows: ctypes.windll.shcore.SetProcessDpiAwareness(1)
   - VOR jedem tkinter Import!
6. Phase 5: Bootstrapper
   REQUIRED_PACKAGES = {"paketname": "import_name"}
   Auto-Installation via subprocess + pip
7. Phase 6: Externe Imports nach Bootstrap
8. Hilfsfunktionen: _lighten(hex, amount), _darken(hex, amount)
9. Tesla Dark Theme Konstanten:
   BG_DARK    = "#1A1A1A"
   BG_CARD    = "#242424"
   BG_INPUT   = "#2E2E2E"
   ACCENT     = "#E31937"
   TEXT_PRI   = "#FFFFFF"
   TEXT_SEC   = "#AAAAAA"
   TEXT_DIM   = "#666666"
   BORDER     = "#3A3A3A"
   SUCCESS    = "#4CAF50"
   WARNING    = "#FF9800"
10. DEFAULT_SETTINGS dict + load_settings() + save_settings()
11. Business-Logik-Klassen (klar getrennt von GUI)
12. Custom Widgets:
    - TBtn: Canvas-basierter Button mit Hover, rounded corners
    - TProgress: Fortschrittsbalken mit Animtion
13. MainApp(tk.Tk):
    - __init__: Fenster-Setup, Widgets erstellen
    - _build_header(): Logo, Titel, Close-Button
    - _build_body(): Haupt-Inhaltsbereich mit Tabs
    - _build_footer(): Status-Bar, Version
14. GlobalExceptionHandler: loggt alle unhandled Exceptions mit traceback
15. if __name__ == "__main__": Block mit try/except

UX-PRINZIPIEN:
- Minimale Klicks — der User soll den Workflow in maximal 3 Schritten abschließen
- Sofortiges visuelles Feedback (Progress-Bar, Status-Meldungen)
- Fehlermeldungen auf Deutsch, klar und handlungsweisend
- Alle Einstellungen persistent (beim nächsten Start geladen)

NACH DER ERSTELLUNG:
1. Führe 10 Code-Iterations-Prüfungen durch (UNI-03)
2. Führe Multi-Agenten-Review durch (UNI-02)
3. Pushe auf GitHub: https://github.com/phunkhazardcrew-svg/[REPO]
```

---

## [MFG-02] TOOL-ERWEITERUNG — NEUE FUNKTION HINZUFÜGEN

**Wann:** Bestehendes Tool soll eine neue Funktionalität bekommen.  
**Usage-Note:** Immer erst die bestehende Architektur vollständig verstehen, DANN Änderungen planen.

```
Erweitere das bestehende Tool [TOOLNAME] um folgende Funktion:

NEUE FUNKTION: [BESCHREIBEN]
BETROFFENE BEREICHE: [KLASSEN / METHODEN wenn bekannt]

VORGEHEN:
1. Lese und analysiere das komplette bestehende Tool
2. Erkläre mir dein Verständnis der Architektur (max. 5 Sätze)
3. Definiere den minimalen Eingriff der die neue Funktion hinzufügt
4. Prüfe Regressions-Risiken: Welche bestehenden Funktionen könnten beeinflusst werden?
5. Implementiere die Änderung
6. Füge Changelog-Eintrag im Header hinzu:
   # v[X.Y] — [DATUM]: [KURZBESCHREIBUNG DER ÄNDERUNG]

KEIN vollständiges Umschreiben außer wenn explizit angefordert.
```

---

## [MFG-03] TOOL-BUGFIX — FEHLER ANALYSIEREN UND BEHEBEN

**Wann:** Ein bestehendes Tool zeigt Fehlerverhalten.  
**Usage-Note:** Erst analysieren, DANN fixen. Keine blinden Reparaturen.

```
Das Tool [TOOLNAME] zeigt folgenden Fehler:

FEHLERBESCHREIBUNG: [WAS PASSIERT]
FEHLERMELDUNG: [EXAKTE FEHLERMELDUNG / TRACEBACK]
REPRODUZIERBAR WENN: [WANN TRITT DER FEHLER AUF]

ANALYSE-VORGEHEN:
1. Lese die relevanten Code-Stellen
2. Identifiziere die Ursache (nicht nur das Symptom!)
3. Erkläre mir die Ursache bevor du fixst
4. Implementiere den minimal-invasiven Fix
5. Erkläre warum der Fix das Problem löst
6. Prüfe ob ähnliche Fehler an anderen Stellen im Code existieren
```

---

## [MFG-04] EXCEL-AUTOMATISIERUNG

**Wann:** Tools die Excel-Dateien verarbeiten, lesen, oder erstellen.  
**Usage-Note:** Entscheiden ob openpyxl (lesen/schreiben) oder win32com (Excel COM, nur Windows) nötig ist.

```
Erstelle Excel-Automatisierung für folgende Aufgabe:

AUFGABE: [BESCHREIBEN]
EXCEL-DATEI: [DATEINAME / STRUKTUR]
RELEVANTE SHEETS: [SHEET-NAMEN]
RELEVANTE SPALTEN: [SPALTEN-BEZEICHNUNGEN]
OUTPUT: [WAS SOLL ENTSTEHEN]

TECHNISCHE ENTSCHEIDUNG:
- Wenn nur Lesen/Schreiben von Daten: openpyxl verwenden
- Wenn Excel-Formeln, Makros, COM-Events nötig: win32com.client
- Wenn Batch-Processing großer Dateien: openpyxl mit read_only=True

Füge Error-Handling für folgende Fälle hinzu:
- Datei nicht gefunden
- Falsches Dateiformat  
- Fehlende/leere Zellen in Pflichtfeldern
- Dateizugriff gesperrt (Excel hat die Datei offen)
```

---

## [MFG-05] STEPDRAWER / PDF-ANALYSE TOOLS

**Wann:** Tools die technische Zeichnungen (STEP, DXF, PDF) verarbeiten.

```
Erstelle/Erweitere ein Tool zur Verarbeitung technischer Zeichnungen.

FORMAT: [STEP / DXF / PDF]
AUFGABE: [BESCHREIBEN — z.B. Dimensionen extrahieren, Features markieren, Berichte generieren]

BIBLIOTHEKEN:
- STEP: cadquery oder pythonocc-core
- DXF: ezdxf
- PDF: pdfplumber (Textextraktion) + PyMuPDF fitz (Rendering)

AUSGABE: [PDF-Bericht / Excel-Liste / JSON-Daten]

Tesla Dark Theme für alle generierten PDF-Reports:
- Hintergrund: #1A1A1A
- Primärtext: #FFFFFF
- Akzent/Titel: #E31937
- Tabellen-Alternating: #1A1A1A / #242424
```

---

## [MFG-06] PYINSTALLER PACKAGING

**Wann:** Ein fertiges Tool soll als standalone .exe für Windows verpackt werden.

```
Verpacke das Tool [TOOLNAME] als Windows .exe mit PyInstaller.

Anforderungen:
1. Single-File .exe (--onefile)
2. Kein Terminal-Fenster (--noconsole für GUI-Tools)
3. Custom Icon einbinden (falls vorhanden): --icon=[PFAD]
4. Alle Ressourcen (JSON, Bilder) in die .exe einbetten
5. Version-Info in der .exe (--version-file)

Erstelle die .spec-Datei und erkläre wie man rebuilt wenn sich das Tool ändert.
Teste ob die .exe auf einem sauberen Windows ohne Python startet.
```

---

## TOOL-REFERENZ (Bisher erstellte Tools)

| Tool | Funktion | Repo |
|------|----------|------|
| StepDrawer.py | STEP→PDF Technische Zeichnungen | phunkhazardcrew-svg/... |
| CAMCode_Ausgabe.py | CAM-Code aus PDF-Arbeitsplänen | phunkhazardcrew-svg/... |
| PDF_Extractor_colouring.py | Feature-Highlighting in Zeichnungen | phunkhazardcrew-svg/... |
| ExcellAutoSaver.py | Batch Excel COM-Automatisierung | phunkhazardcrew-svg/... |
| Tool_Name (Werkzeugdatenbank) | Tebis/HyperMILL Tool-Datenbank-Sync | phunkhazardcrew-svg/Tool_Name |

---

*Bereich 01 | Manufacturing Tools | Stand April 2026*
