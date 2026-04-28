# 🏭 BEREICH 02: CNC & CAM
**Archiv:** PROMTS | **Letztes Update:** April 2026  
**Zugehörige Skills:** `hypermill-vt-advisor`, `hypermill-automation`

---

## [CNC-01] HYPERMILL VT MAKRO — NEUENTWICKLUNG

**Wann:** Neues Virtual Tool Makro im HyperMILL VT-Editor erstellen.  
**Usage-Note:** Dieser Prompt gibt Führung durch den GUI-Prozess, keine direkten Code-Blöcke.

```
Ich möchte ein neues HyperMILL Virtual Tool (VT) Makro entwickeln.

ANWENDUNGSFALL: [BESCHREIBEN — z.B. Tiefbohrung >8.5xD mit Pecking-Zyklus]
MASCHINEN-TYP: [MASCHINENTYP / KINEMATIK]
CONTROLLER: Heidenhain TNC7
HYPERMILL-VERSION: [VERSION]

Führe mich durch:
1. Suchfilter-Konfiguration im VT-Editor (TOOL_SEARCH Parameter)
2. Feature-Variablen und Connector-Variablen die relevant sind
3. Makro-Sequenz mit allen Schritten in Reihenfolge
4. Entscheidungslogik (wenn Tiefe > Schwellwert DANN...)
5. TRANSFER_TO_CYCLE für korrekten Bohrzyklus
6. Test-Workflow: Wie prüfe ich das Makro auf einer einfachen Bohrung?

Wichtige Tiefenschwellen für Bohrer:
- Standard: <5xD
- Tief: 5–8.5xD
- Sehr tief: >8.5xD → Pecking-Zyklus zwingend
```

---

## [CNC-02] HYPERMILL AUTOMATION CENTER — PYTHON SKRIPT

**Wann:** Python-Skript für Automation Center basierend auf Excel-Arbeitsplan.

```
Entwickle ein Python-Skript für das HyperMILL Automation Center.

AUFGABE: [BESCHREIBEN]
EXCEL-DATEI: [DATEINAME]
RELEVANTE SPALTEN: [SPALTEN-NAMEN / INDIZES]
AUSGABE: [NC-PROGRAMM / WERKZEUGPFAD / REPORT]

CODE-ANFORDERUNGEN:
- Vollständige Kommentierung jeder Funktion (anfängerfreundlich)
- Excel-Einlesen mit openpyxl
- Fehlerbehandlung für fehlende/fehlerhafte Einträge
- Logging aller Verarbeitungsschritte
- Fortschrittsanzeige für lange Batch-Prozesse

NACH DER ERSTELLUNG:
- 10 Iterations-Prüfung (UNI-03)
- Multi-Agenten-Review (UNI-02)
```

---

## [CNC-03] WERKZEUGDATENBANK ANALYSE

**Wann:** Tool-Datenbank zwischen Tebis und HyperMILL abgleichen oder Werkzeuge analysieren.

```
Analysiere / Synchronisiere die Werkzeugdatenbank.

AUFGABE: [Abgleich / Import / Export / Analyse]
QUELLE: [Tebis / HyperMILL / Zoller / Excel]
ZIEL: [Tebis / HyperMILL / Excel / PDF-Report]

Relevante Parameter pro Werkzeug:
- Typ (Bohrer, Fräser, Reibahle, Gewindeschneider)
- Durchmesser, Spitzenlänge (reach), Ausspannlänge (AL)
- Verwendungszweck (Schruppen / Schlichten / Bohren etc.)
- Material-Klasse
- Beschichtung

Prüfe auf: Duplikate, fehlende Pflichtfelder, inkonsistente Bezeichnungen.
Erstelle einen Abweichungsbericht.
```

---

## [CNC-04] NC-CODE REVIEW

**Wann:** NC-Programme für Heidenhain TNC7 prüfen oder optimieren.

```
Reviewe folgenden NC-Code für Heidenhain TNC7:

[CODE HIER]

Bauteil-Kontext:
- Material: [MATERIAL]
- Operation: [SCHRUPPEN/SCHLICHTEN/BOHREN/etc.]
- Spannlage: [SPANNLAGE]
- Maschine: [MASCHINENTYP]

Prüfpunkte:
1. TNC7-Syntax-Konformität
2. Sicherheitsebenen korrekt gesetzt?
3. Kollisionsrisiken (Spannmittel, Nullpunkt-Verschiebungen)
4. Schnittparameter sinnvoll für Material?
5. Optimierungspotenzial (Verfahrwege, Zustellungen)
6. Fehlende Sicherheitsabschaltungen

Ausgabe: Gefundene Probleme mit Zeile + Korrekturvorschlag.
```

---

*Bereich 02 | CNC & CAM | Stand April 2026*
