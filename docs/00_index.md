# Dokumentenindex: Bienenapp (BSK-App)

**Projekt:** Bienenapp - Digitale Stockkartenverwaltung  
**Dokument:** Zentrale Dokumentenübersicht  
**Version:** 1.0  
**Datum:** 2024-03-28  
**Letztes Update:** 2024-03-28  

---

## Über dieses Dokument

Dies ist der zentrale Index aller Projektdokumente. Hier findest du:
- Übersicht aller vorhandenen Dokumente
- Status der Dokumentation (fertig/in Arbeit/geplant)
- Kurzbeschreibung und Verlinkung
- Schnellen Einstieg für neue Teammitglieder und KI-Tools (Claude Code)

**Legende:**
- ✅ Fertig / Freigegeben
- 🚧 In Arbeit
- ⬜ Geplant / Noch nicht gestartet
- ❌ Verworfen / Nicht relevant

---

## Projektdokumentation

### Root-Ebene

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ⬜ | `README.md` | Projekt-Übersicht, Quick-Start Guide |
| ⬜ | `.gitignore` | Git-Ausschlüsse (node_modules, build/, etc.) |
| ⬜ | `LICENSE` | Lizenzinformation (MIT/GPL/Proprietär) |
| 🚧 | `00_index.md` | Dieses Strukturdokument |

---

## Phase 0: Projektsetup

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ✅ | `docs/01_projektsteckbrief.md` | Projektziele, Stakeholder, Zeitplan |
| ⬜ | `docs/02_projektplan.md` | Detaillierter Projektplan mit Meilensteinen |
| ⬜ | `docs/03_stakeholder_analyse.md` | Stakeholder-Matrix, Interessen, Kommunikation |
| ⬜ | `docs/04_risikoanalyse.md` | Risk Management, Gegenmaßnahmen |

---

## Phase 1: Requirements

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ⬜ | `docs/05_requirements/REQ_overview.md` | Überblick aller Requirements |
| ⬜ | `docs/05_requirements/REQ_behoerden.md` | Veterinäramt-Vorgaben, Verordnungen |
| ⬜ | `docs/05_requirements/REQ_funktional.md` | Funktionale Anforderungen (User Stories) |
| ⬜ | `docs/05_requirements/REQ_nichtfunktional.md` | Performance, Security, Usability |
| ⬜ | `docs/05_requirements/REQ_traceability.xlsx` | Verlinkung REQs ↔ Tests (optional) |

---

## Phase 2: Konzept

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ⬜ | `docs/06_konzept/software_architektur.md` | Blockschaltbild, Komponenten, Schnittstellen |
| ⬜ | `docs/06_konzept/datenmodell.md` | ER-Diagramm, Tabellen, Beziehungen |
| ⬜ | `docs/06_konzept/technologie_entscheidung.md` | Flutter vs React Native vs PWA |
| ⬜ | `docs/06_konzept/ui_mockups/mockup_beschreibung.md` | UI/UX-Konzept, Wireframes |
| ⬜ | `docs/06_konzept/ui_mockups/screen_01_hauptmenu.png` | Mockup: Hauptmenü |
| ⬜ | `docs/06_konzept/ui_mockups/screen_02_stockkarte.png` | Mockup: Stockkarten-Erfassung |

---

## Phase 3: Detaildesign

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ⬜ | `docs/07_detaildesign/api_spezifikation.md` | REST/GraphQL API zwischen App & DB |
| ⬜ | `docs/07_detaildesign/datenbank_schema.sql` | SQL-Schema für Heim-Datenbank |
| ⬜ | `docs/07_detaildesign/sync_konzept.md` | Synchronisations-Logik, Konfliktauflösung |
| ⬜ | `docs/07_detaildesign/druckmodul_spezifikation.md` | PDF-Generierung aus DB-Daten |

---

## Phase 4: Testing

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ⬜ | `docs/08_testing/testplan.md` | Teststrategie, Testumgebung, Testziele |
| ⬜ | `docs/08_testing/testcases.md` | Manuelle & automatisierte Testfälle |
| ⬜ | `docs/08_testing/testreport_template.md` | Vorlage für Testergebnisse |

---

## Phase 5: Benutzer-Dokumentation

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ⬜ | `docs/09_benutzerhandbuch/anleitung_app.md` | Wie bediene ich die App? (Endnutzer) |
| ⬜ | `docs/09_benutzerhandbuch/anleitung_sync.md` | Datensynchronisation einrichten |
| ⬜ | `docs/09_benutzerhandbuch/faq.md` | Häufig gestellte Fragen |

---

## Phase 6: Projektabschluss

| Status | Dokument | Beschreibung |
|--------|----------|--------------|
| ⬜ | `docs/10_projektabschluss/lessons_learned.md` | Was lief gut? Was kann besser werden? |
| ⬜ | `docs/10_projektabschluss/wartungsplan.md` | Support-Strategie, Update-Zyklen |
| ⬜ | `docs/10_projektabschluss/changelog.md` | Versionshistorie (v1.0, v1.1, ...) |

---

## Source Code (`src/`)

*Wird während der Implementierungsphase gefüllt. Struktur siehe `projektordnerstruktur.md`*

| Status | Bereich | Beschreibung |
|--------|---------|--------------|
| ⬜ | `src/app/` | Mobile App (Flutter/React Native/PWA) |
| ⬜ | `src/database/` | Datenbank-Schemas, Migrations |
| ⬜ | `src/sync/` | Synchronisations-Logik |

---

## Tests (`tests/`)

| Status | Bereich | Beschreibung |
|--------|---------|--------------|
| ⬜ | `tests/unit/` | Unit-Tests (Funktionen, Module) |
| ⬜ | `tests/integration/` | Integrationstests (App ↔ DB) |
| ⬜ | `tests/e2e/` | End-to-End Tests (Nutzerszenarien) |

---

## Assets & Tools

| Status | Bereich | Beschreibung |
|--------|---------|--------------|
| ⬜ | `assets/icons/` | App-Icons (verschiedene Größen) |
| ⬜ | `assets/templates/` | PDF-Templates für Stockkarten-Druck |
| ⬜ | `tools/` | Hilfstools (DB-Viewer, PDF-Generator, etc.) |

---

## Releases

| Status | Version | Beschreibung |
|--------|---------|--------------|
| ⬜ | `releases/beta/` | Beta-Versionen für Tester |
| ⬜ | `releases/v1.0.0/` | Erste produktive Version |

---

## Schnellzugriff: Wichtigste Dokumente

**Für Projektleitung:**
1. `docs/01_projektsteckbrief.md` → Projektziele & Status
2. `docs/02_projektplan.md` → Zeitplanung & Meilensteine
3. `docs/04_risikoanalyse.md` → Risiken im Blick behalten

**Für Entwicklung:**
1. `docs/05_requirements/REQ_funktional.md` → Was soll gebaut werden?
2. `docs/06_konzept/software_architektur.md` → Wie ist das System aufgebaut?
3. `docs/07_detaildesign/api_spezifikation.md` → Technische Schnittstellen

**Für Testing:**
1. `docs/08_testing/testplan.md` → Was wird getestet?
2. `docs/08_testing/testcases.md` → Wie wird getestet?

**Für Endnutzer:**
1. `docs/09_benutzerhandbuch/anleitung_app.md` → App-Bedienung
2. `docs/09_benutzerhandbuch/faq.md` → Probleme & Lösungen

---

## Für Claude Code: Kontext-Einstieg

**Wenn du als KI-Tool dieses Projekt übernimmst:**

1. **Lies zuerst:** `README.md` (Projektübersicht)
2. **Dann:** `docs/01_projektsteckbrief.md` (Ziele & Scope)
3. **Requirements:** Alles in `docs/05_requirements/`
4. **Architektur:** `docs/06_konzept/software_architektur.md`
5. **Code:** `src/` (siehe Ordnerstruktur)

**Wichtige Constraints:**
- Offline-First: App muss ohne Internet funktionieren
- Behörden-Konformität: Veterinäramt-Vorgaben beachten
- Datensicherheit: Keine Datenverluste bei Sync

---

## Versionierung dieses Index

| Version | Datum | Änderung |
|---------|-------|----------|
| 1.0 | 2024-03-28 | Initiale Erstellung (Ordnerstruktur angelegt) |

---

**Hinweis:** Dieser Index wird laufend aktualisiert. Nach jedem Meilenstein Status aktualisieren!

**Nächster Review:** Nach Fertigstellung von Phase 1 (Requirements)

