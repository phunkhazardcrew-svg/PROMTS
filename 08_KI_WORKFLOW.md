# 🤖 BEREICH 08: KI-WORKFLOW & TECHNIK
**Archiv:** PROMTS | **Letztes Update:** April 2026

---

## [KI-01] MULTI-KI-WORKFLOW PLANUNG

**Wann:** Aufgaben die mehrere KI-Systeme kombinieren.

```
Plane den optimalen Multi-KI-Workflow für:

AUFGABE: [BESCHREIBEN]
DEADLINE: [WENN RELEVANT]

VERFÜGBARE SYSTEME:
- Claude Sonnet (claude.ai / API) — Reasoning, Schreiben, Code-Review
- Claude Code (Terminal) — Autonomes Coden, Dateioperationen
- DeepSeek V4 (API / Open WebUI) — Günstige Code-Generierung
- Gemini Flash/Pro — Lange Kontextfenster, Multimodal
- Ollama lokal (NiPoGi P1) — Offline, Privacy-sensitive Tasks

BEWERTUNGSKRITERIEN:
- Kosten (welches System für welche Teilaufgabe am günstigsten)
- Qualität (welches System am besten für diese Art Aufgabe)
- Latenz (was muss schnell sein)
- Datenschutz (was darf nicht zu externen APIs)

AUSGABE:
1. Aufgaben-Aufteilung nach System
2. Datenfluss-Diagramm (welches System übergibt was an wen)
3. Konkrete API-Calls oder Kommandos
4. Geschätzte Kosten
```

---

## [KI-02] OPEN WEBUI / LOKALES KI-SETUP

**Wann:** Lokale KI-Umgebung auf dem NiPoGi Pinova P1 (Windows 11) aufsetzen oder erweitern.

```
Hilf mir mit meinem lokalen KI-Setup auf dem NiPoGi Pinova P1.

HARDWARE: NiPoGi Pinova P1 | AMD Ryzen 4300U | 16GB RAM | Keine dedizierte GPU | Windows 11

AUFGABE: [BESCHREIBEN — z.B. Open WebUI installieren, DeepSeek verbinden, Google Drive Integration]

ANFORDERUNGEN:
- Alles über Docker Desktop (kein direktes Linux erforderlich)
- PowerShell als Terminal
- Alle Befehle für Windows angepasst (Pfade mit C:\, Backtick für Zeilenumbrüche)
- Autostart über Docker Desktop on Windows
- Kostenrahmen: möglichst unter $5/Monat API-Kosten

ERKLÄRE:
1. Schritt-für-Schritt auf Deutsch
2. Was jeder Schritt macht und warum
3. Troubleshooting für häufige Fehler
4. Wie ich das Setup nach einem PC-Neustart starte
```

---

## [KI-03] CLAUDE ARTIFACT / REACT COMPONENT BAUEN

**Wann:** Interaktive Artifacts, React Components, oder HTML-Tools erstellen.

```
Erstelle ein [React Artifact / HTML Tool / Interaktive Visualisierung].

ZWECK: [BESCHREIBEN]
DATEN: [WELCHE DATEN / INPUTS]
AUSGABE: [WELCHE AUSGABE / VISUALISIERUNG]

TECHNISCHE ANFORDERUNGEN:
- Tailwind CSS (nur Core Utility Classes — kein Compiler!)
- Keine localStorage / sessionStorage (nicht unterstützt)
- State mit useState/useReducer
- Verfügbare Libraries: recharts, lucide-react, lodash, d3, three.js
- Single-File (JSX + CSS in einer Datei)
- Vollständig responsiv

DESIGN-ANSPRUCH: Professionell, clean — kein "generischer KI-Look".
Verwende dunkle Themes wenn zum Kontext passend.

NACH FERTIGSTELLUNG: 10 Iterations-Prüfung auf alle Fehlerarten.
```

---

*Bereich 08 | KI-Workflow & Technik | Stand April 2026*
