# 🐙 BEREICH 09: GITHUB & VERSIONSKONTROLLE
**Archiv:** PROMTS | **Letztes Update:** April 2026  
**GitHub:** https://github.com/phunkhazardcrew-svg  
**Token:** [TOKEN_REDACTED]

---

## [GIT-01] REPOSITORY ANALYSIEREN UND REPARIEREN

**Wann:** Ein GitHub-Repo hat Probleme oder soll analysiert werden.

```
Analysiere das GitHub-Repository und behebe das Problem.

REPO: https://github.com/phunkhazardcrew-svg/[REPO-NAME]
TOKEN: [TOKEN_REDACTED]

PROBLEM: [BESCHREIBEN]

VORGEHEN:
1. Klone das Repo (git clone mit Token-Auth)
2. Prüfe alle relevanten Dateien
3. Verstehe die Gesamtarchitektur
4. Identifiziere das Problem + Ursache
5. Implementiere Fix (10 Iterations-Prüfung!)
6. Test: Läuft alles wie erwartet?
7. Commit: [type](scope): Präzise Beschreibung
8. Push auf main
9. Optional: Tag setzen wenn Meilenstein

COMMIT-TYPES: feat, fix, docs, refactor, test, chore, perf
```

---

## [GIT-02] CHECKPOINT / TAG ERSTELLEN

**Wann:** Vor größeren Änderungen oder nach wichtigen Meilensteinen.

```
Erstelle einen Git-Checkpoint für:

REPO: [REPO-URL]
ANLASS: [MEILENSTEIN-BESCHREIBUNG]
TAG-NAME: [sprechender-tag-name] (z.B. "al-bug-fixed", "session-2026-04-28-complete")

AKTIONEN:
1. Alle nicht-committeten Änderungen committen
2. Aussagekräftiger Commit: "checkpoint: [KURZBESCHREIBUNG]"
3. Tag erstellen: git tag -a [TAG-NAME] -m "[BESCHREIBUNG]"
4. Tag pushen: git push origin [TAG-NAME]
5. In CHECKPOINT.md oder README Changelog-Eintrag ergänzen

ZIEL: Jeder Tag ist ein Rollback-Punkt. Beschreibe klar was er enthält.
Token: [TOKEN_REDACTED]
```

---

## [GIT-03] DIFF-ANALYSE (MANUELLE ÄNDERUNGEN VERSTEHEN)

**Wann:** Wenn Dateien manuell verändert wurden und ich wissen will was sich geändert hat.

```
Analysiere was sich in diesem Repo verändert hat.

REPO: https://github.com/phunkhazardcrew-svg/[REPO-NAME]
VERÄNDERTE DATEIEN: [ORDNER/DATEIPFADE]
TOKEN: [TOKEN_REDACTED]

AUFGABE:
1. Lade die veränderten Dateien
2. Vergleiche mit dem vorherigen Stand (git diff oder manuell)
3. Erkläre mir in klarem Deutsch was geändert wurde
4. Erkläre WARUM diese Änderung gemacht wurde (deine Interpretation)
5. Prüfe ob die Änderungen Sinn ergeben oder Probleme verursachen könnten
6. Empfehle nächste Schritte (Merge, Test, etc.)
```

---

## [GIT-04] NEUES REPOSITORY AUFSETZEN

**Wann:** Für neue Projekte ein GitHub-Repository anlegen und einrichten.

```
Richte ein neues GitHub-Repository für folgendes Projekt ein:

PROJEKT-NAME: [NAME]
BESCHREIBUNG: [KURZE BESCHREIBUNG]
ÖFFENTLICH / PRIVAT: [PUBLIC / PRIVATE]
SPRACHE / TECH-STACK: [TECH]

SETUP-AUFGABEN:
1. Erstelle lokale Projektstruktur mit sinnvoller Ordnerarchitektur
2. Erstelle README.md mit: Beschreibung, Installation, Usage, Roadmap
3. Erstelle .gitignore für [TECH-STACK]
4. Erstelle CHANGELOG.md mit initialer Version
5. Initialer Commit: "feat: initial project setup"
6. Push auf GitHub (neues Repo erstellen via API oder manuell)
7. Branch-Schutz für main: keine direkten Pushes (optional)

TOKEN: [TOKEN_REDACTED]
GITHUB USER: phunkhazardcrew-svg
```

---

*Bereich 09 | GitHub & Versionskontrolle | Stand April 2026*
