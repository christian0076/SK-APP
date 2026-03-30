# Projektplan: Bienenapp (BSK-App)

**Projekt:** Bienenapp - Digitale Stockkartenverwaltung  
**Dokument:** Detaillierter Projektplan  
**Version:** 1.0  
**Datum:** 2024-03-28  
**Projektleiter:** [Dein Name]  
**Status:** In Arbeit  

---

## 1. Projektübersicht

### 1.1 Projektziel
Entwicklung einer mobilen App zur digitalen Erfassung von Bienenvolk-Stockkarten mit Offline-Funktionalität, Datenbankanbindung und Druckfunktion für behördenkonforme Dokumentation.

**Verweis:** Detaillierte Ziele siehe `docs/01_projektsteckbrief.md`

### 1.2 Scope

#### ✅ Im Scope (Was wird gemacht)
- Mobile App (Android, evtl. iOS oder PWA)
- Offline-Dateneingabe im Bienenstand
- Lokale Datenbank auf Mobilgerät
- Heim-Datenbank (PC/Server)
- Synchronisationsmechanismus (WLAN/USB/Cloud)
- PDF-Druckfunktion für Stockkarten
- Einhaltung veterinärrechtlicher Vorgaben
- Beta-Testing mit realen Völkern
- Dokumentation (technisch + Endnutzer)

#### ❌ Out of Scope (Was wird NICHT gemacht)
- Multi-User-System (erstmal Single-User)
- Cloud-Backend mit Abo-Modell (evtl. Version 2.0)
- iOS-Version (falls zu aufwendig, dann nur Android im MVP)
- Integration mit Imker-Software von Drittanbietern
- Automatische Wetter-Daten-Integration
- KI-gestützte Krankheitserkennung (nice-to-have für später)

### 1.3 Erfolgskriterien
1. App erfasst alle Pflichtfelder gemäß Veterinäramt-Vorgaben
2. Offline-Betrieb funktioniert ohne Datenverlust
3. Sync-Prozess ist fehlerfrei und konfliktfrei
4. Gedruckte Stockkarten entsprechen behördlichen Anforderungen
5. Beta-Tester bewerten Usability mit ≥ 4/5 Sternen
6. Projekt abgeschlossen in max. 3 Monaten (MVP)

---

## 2. Stakeholder & Kommunikation

### 2.1 Stakeholder-Matrix

| Stakeholder | Rolle | Interesse | Einfluss | Kommunikation |
|-------------|-------|-----------|----------|---------------|
| Du (Projektleiter & Entwickler) | Owner | Hoch | Hoch | Täglich (Selbstreflexion) |
| Claude AI | Planungs-Support | Mittel | Mittel | Bei Bedarf (Planung, Konzept) |
| Claude Code | Entwicklungs-Support | Mittel | Mittel | Ab Phase 4 (Implementierung) |
| Veterinäramt | Behörde | Hoch | Hoch | Einmalig (REQ-Klärung) |
| Imkerkollegen (Beta) | Tester | Mittel | Niedrig | Wöchentlich während Beta-Phase |
| Familie/Freunde | Indirekt Betroffene | Niedrig | Niedrig | Bei Meilensteinen informieren |

### 2.2 Kommunikationsplan

| Was | Wer | Wie oft | Medium |
|-----|-----|---------|--------|
| Projektstatus | Selbstreflexion | Wöchentlich | Statusnotiz in `changelog.md` |
| Requirement-Klärung | Veterinäramt | Einmalig (Phase 2) | E-Mail/Telefonat |
| Beta-Feedback | Tester | Wöchentlich | Fragebogen/Interview |
| Meilenstein-Review | Selbst + Claude | Nach jedem Gate | Dokumentierte Entscheidung |

### 2.3 Eskalationspfad

Da Solo-Projekt: **Selbsteskalation bei Blockern**
- Problem identifizieren → Risiko-Log aktualisieren
- Lösungsoptionen mit Claude diskutieren
- Entscheidung dokumentieren im Entscheidungslog

---

## 3. Phasenplanung

### 3.1 Übersicht der Projektphasen

Das Projekt folgt einem **iterativen Phasenmodell mit Gates**. 

**Wichtig:** Nach jedem Gate-Review kann **zurück in frühere Phasen gesprungen** werden, falls:
- Requirements unvollständig/unklar sind
- Technische Machbarkeit anzuzweifeln ist
- Risiken sich materialisieren
- Stakeholder-Anforderungen ändern


### 3.2 Phasenbeschreibung

#### Phase 0: Planung (Setup)

**Ziel:** Projekt aufsetzen, Rahmenbedingungen klären

**Hauptaktivitäten:**

- Projektsteckbrief erstellen ✅
- Projektplan schreiben 🚧
- Ordnerstruktur anlegen ✅
- Git-Repository initialisieren
- Stakeholder-Analyse
- Tool-Stack-Entscheidung

**Deliverables:**

- Projektsteckbrief
- Projektplan
- Ordnerstruktur
- Risiko-Übersicht

**Gate 0 Exit-Kriterien:**

- Projektziel klar definiert
- Ressourcen (Zeit, Tools) verfügbar
- Go-Entscheidung vom Projektleiter

---

#### Phase 1: Requirements Capture

**Ziel:** Alle Anforderungen erfassen und validieren

**Hauptaktivitäten:**

- Veterinäramt-Verordnungen recherchieren
- Pflichtfelder für Stockkarten ermitteln
- Funktionale Requirements ableiten
- Nicht-funktionale Requirements definieren
- Requirements priorisieren (MoSCoW)
- Traceability-Matrix anlegen

**Deliverables:**

- `REQ_behoerden.md` (Behördenanforderungen)
- `REQ_funktional.md` (User Stories)
- `REQ_nichtfunktional.md` (Performance, Security)
- `REQ_overview.md` (Gesamt-Übersicht)

**Gate 1 Exit-Kriterien:**

- ✅ Alle Must-Have REQs identifiziert
- ✅ Veterinäramt-Anforderungen geklärt
- ✅ REQs sind testbar formuliert
- ✅ Keine offenen Fragen bei kritischen REQs

**Rücksprung-Trigger:**

- Unklare/widersprüchliche Anforderungen → Stakeholder klären

---

#### Phase 2: Konzept

**Ziel:** Technisches Konzept & Architektur erstellen

**Hauptaktivitäten:**

- Software-Architektur entwerfen (Blockdiagramm)
- Datenmodell (ER-Diagramm) erstellen
- Technologie-Entscheidung (Flutter/React Native/PWA)
- UI/UX-Mockups erstellen
- Prototyp einzelner Komponenten testen
- Schnittstellen definieren (App ↔ DB)

**Deliverables:**

- `software_architektur.md`
- `datenmodell.md`
- `technologie_entscheidung.md`
- UI-Mockups (Wireframes)

**Gate 2 Exit-Kriterien:**

- ✅ Architektur ist konsistent
- ✅ Technologie-Stack festgelegt
- ✅ Datenmodell deckt alle REQs ab
- ✅ Mockups von Stakeholder (du) abgenommen

**Rücksprung-Trigger:**

- Neue REQs entdeckt → zurück zu Phase 1
- Technische Machbarkeit zweifelhaft → REQs anpassen (Phase 1)

---

#### Phase 3: Detaildesign

**Ziel:** Implementierungsreife Spezifikationen erstellen

**Hauptaktivitäten:**

- API-Spezifikation (REST/GraphQL)
- Datenbank-Schema (SQL) detaillieren
- Sync-Konzept ausarbeiten
- Druckmodul spezifizieren
- Test Cases gegen REQs schreiben

**Deliverables:**

- `api_spezifikation.md`
- `datenbank_schema.sql`
- `sync_konzept.md`
- `druckmodul_spezifikation.md`
- `testcases.md` (initial)

**Gate 3 Exit-Kriterien:**

- ✅ Alle Specs sind implementierbar
- ✅ Test Cases für alle Must-Have REQs vorhanden
- ✅ Keine offenen technischen Fragen

**Rücksprung-Trigger:**

- Design-Inkonsistenzen → zurück zu Phase 2
- REQ-Lücken entdeckt → zurück zu Phase 1

---

#### Phase 4: Implementation & Integration

**Ziel:** Lauffähige Software entwickeln

**Hauptaktivitäten:**

- App-Entwicklung (Frontend + lokale DB)
- Heim-Datenbank aufsetzen
- Sync-Mechanismus implementieren
- Druckmodul (PDF-Generierung) entwickeln
- Unit-Tests schreiben & ausführen
- Integrationstests (App ↔ DB)

**Deliverables:**

- Lauffähige App (APK/IPA/PWA)
- Datenbank mit Testdaten
- Funktionierendes Sync-System
- Test-Reports (Unit + Integration)

**Gate 4 Exit-Kriterien:**

- ✅ Alle Must-Have Features implementiert
- ✅ Unit-Tests bestanden (>80% Coverage)
- ✅ Integrationstests erfolgreich
- ✅ App läuft auf Testgerät

**Rücksprung-Trigger:**

- Implementierung unmöglich → zurück zu Phase 3 (Design anpassen)
- REQ-Änderungen → zurück zu Phase 1

---

#### Phase 5: Verification & Validation (V&V)

**Ziel:** Systematisches Testen gegen alle Requirements

**Hauptaktivitäten:**

- Alle Test Cases abarbeiten
- End-to-End Tests (Nutzerszenarios)
- Performance-Tests (Offline-Betrieb, Sync-Geschwindigkeit)
- Usability-Tests (selbst durchführen)
- Bug-Fixing
- Regression-Tests nach Fixes

**Deliverables:**

- Vollständiger Test-Report
- Bug-Liste (mit Status: fixed/open)
- Abnahmeprotokoll (Selbstabnahme)

**Gate 5 Exit-Kriterien:**

- ✅ Alle kritischen Bugs behoben
- ✅ Mind. 95% der Test Cases bestanden
- ✅ Performance-Ziele erreicht
- ✅ Keine Blocker mehr offen

**Rücksprung-Trigger:**

- Schwere Bugs → zurück zu Phase 4 (Implementierung)
- Design-Fehler → zurück zu Phase 3
- REQ-Missverständnisse → zurück zu Phase 1

---

#### Phase 6: Beta-Phase

**Ziel:** Feldtest mit echten Daten und Nutzern

**Hauptaktivitäten:**

- Beta-Version an 2-3 Imker verteilen
- Reale Stockkarten-Daten erfassen
- Wöchentliches Feedback sammeln
- Usability-Probleme identifizieren
- Minor Bugfixes
- Dokumentation verfeinern

**Deliverables:**

- Beta-Feedback-Report
- Überarbeitete App (v0.9)
- Finales Benutzerhandbuch

**Gate 6 Exit-Kriterien:**

- ✅ Beta-Tester bewerten ≥ 4/5
- ✅ Keine kritischen Bugs gemeldet
- ✅ Dokumentation vollständig

**Rücksprung-Trigger:**

- Gravierende Usability-Probleme → zurück zu Phase 2 (UI-Überarbeitung)
- Neue Must-Have REQs → zurück zu Phase 1

---

#### Phase 7: Release

**Ziel:** App produktiv machen

**Hauptaktivitäten:**

- Finale Version bauen (v1.0)
- App-Store-Listing vorbereiten (falls relevant)
- Download-Seite einrichten
- Release Notes schreiben
- Marketing (optional: Imker-Forum, Verein)

**Deliverables:**

- Produktive App v1.0
- Release Notes
- Download-Link / App-Store-Eintrag

**Gate 7 Exit-Kriterien:**

- ✅ App ist öffentlich verfügbar
- ✅ Dokumentation für Endnutzer vorhanden
- ✅ Support-Kanal definiert (E-Mail, Forum)

---

#### Phase 8: Service & Wartung

**Ziel:** Langfristige Betreuung

**Hauptaktivitäten:**

- Bug-Reports bearbeiten
- Minor Updates (Bugfixes)
- Feature-Requests sammeln (für v2.0)
- Backup-Strategie überwachen

**Deliverables:**

- Wartungsplan
- Changelog (laufend aktualisiert)
- Update-Releases (v1.1, v1.2, ...)

**Laufend, kein Gate**

---


### 3.3 Phasen-Abhängigkeiten

| Phase | Muss abgeschlossen sein vor... | Besonderheit |
|-------|-------------------------------|--------------|
| Phase 0: Planung | Phase 1 | Projekt-Setup |
| Phase 1: Requirements | Phase 2 | Gate 1: REQs vollständig |
| Phase 2: Konzept | Phase 3 | Gate 2: Architektur freigegeben |
| Phase 3: Detaildesign | Phase 4 | Gate 3: Specs implementierbar |
| Phase 4: Implementation | Phase 5 | Gate 4: Code läuft |
| Phase 5: V&V | Phase 6 | Gate 5: Tests bestanden |
| Phase 6: Beta | Phase 7 | Gate 6: Feldtest erfolgreich |
| Phase 7: Release | Phase 8 | Gate 7: App produktiv |
| Phase 8: Service | - | Läuft parallel zu v2.0-Entwicklung |


**Parallel laufend in allen Phasen:**
- Risk Management
- Change Management
- Dokumentation

---

## 4. Meilensteine

| Nr. | Meilenstein | Phase | Geplantes Datum | Deliverables | Status |
|-----|-------------|-------|----------------|--------------|--------|
| M0 | Projekt-Kickoff | 0 | 2024-03-28 | Projektsteckbrief, Ordnerstruktur | ✅ |
| M1 | Projektplan fertig | 0 | 2024-04-05 | Projektplan, Tool-Auswahl | 🚧 |
| M2 | Requirements finalisiert | 1 | 2024-04-15 | Alle REQ-Docs, Gate 1 bestanden | ⬜ |
| M3 | Konzept abgenommen | 2 | 2024-04-30 | Architektur, Mockups, Gate 2 bestanden | ⬜ |
| M4 | Detaildesign review | 3 | 2024-05-10 | Alle Specs, Test Cases, Gate 3 bestanden | ⬜ |
| M5 | Erster lauffähiger Prototyp | 4 | 2024-05-30 | App + DB funktionieren, Gate 4 bestanden | ⬜ |
| M6 | V&V abgeschlossen | 5 | 2024-06-10 | Alle Tests bestanden, Gate 5 bestanden | ⬜ |
| M7 | Beta-Phase abgeschlossen | 6 | 2024-06-25 | Beta-Feedback verarbeitet, Gate 6 bestanden | ⬜ |
| M8 | Release v1.0 | 7 | 2024-06-30 | App produktiv, Gate 7 bestanden | ⬜ |

**Kritischer Pfad:** M0 → M1 → M2 → M3 → M4 → M5 → M6 → M7 → M8

---

## 5. Arbeitspakete (Work Breakdown Structure)

*Hinweis: Wird detailliert pro Phase gefüllt. Hier Übersicht:*

### Phase 0: Planung
- [ ] AP 0.1: Projektsteckbrief erstellen (2h) ✅
- [ ] AP 0.2: Ordnerstruktur definieren & anlegen (1h) ✅
- [ ] AP 0.3: Projektplan schreiben (5h) 🚧
- [ ] AP 0.4: Git-Repository initialisieren (0.5h)
- [ ] AP 0.5: Tool-Stack festlegen (2h)
- [ ] AP 0.6: Risiko-Übersicht erstellen (2h)

**Gesamt Phase 0:** ca. 12.5h

### Phase 1: Requirements
- [ ] AP 1.1: Veterinäramt kontaktieren (1h)
- [ ] AP 1.2: Verordnungen recherchieren (3h)
- [ ] AP 1.3: Behörden-REQs dokumentieren (2h)
- [ ] AP 1.4: Funktionale REQs ableiten (4h)
- [ ] AP 1.5: Nicht-funktionale REQs definieren (2h)
- [ ] AP 1.6: REQs priorisieren (MoSCoW) (1h)
- [ ] AP 1.7: REQ-Übersicht erstellen (1h)
- [ ] AP 1.8: Gate 1 Review durchführen (1h)

**Gesamt Phase 1:** ca. 15h

### Phase 2: Konzept
- [ ] AP 2.1: Architektur-Blockdiagramm (3h)
- [ ] AP 2.2: Datenmodell (ER-Diagramm) (3h)
- [ ] AP 2.3: Technologie-Recherche (Flutter/PWA/etc.) (4h)
- [ ] AP 2.4: Technologie-Entscheidung dokumentieren (1h)
- [ ] AP 2.5: UI-Mockups erstellen (5h)
- [ ] AP 2.6: Prototyp testen (optional) (3h)
- [ ] AP 2.7: Gate 2 Review (1h)

**Gesamt Phase 2:** ca. 20h

### Phase 3: Detaildesign
- [ ] AP 3.1: API-Spezifikation schreiben (3h)
- [ ] AP 3.2: DB-Schema (SQL) detaillieren (3h)
- [ ] AP 3.3: Sync-Konzept ausarbeiten (4h)
- [ ] AP 3.4: Druckmodul spezifizieren (2h)
- [ ] AP 3.5: Test Cases erstellen (5h)
- [ ] AP 3.6: Gate 3 Review (1h)

**Gesamt Phase 3:** ca. 18h

### Phase 4: Implementation
- [ ] AP 4.1: Entwicklungsumgebung aufsetzen (2h)
- [ ] AP 4.2: Datenbank implementieren (5h)
- [ ] AP 4.3: App-Frontend entwickeln (20h)
- [ ] AP 4.4: Sync-Modul entwickeln (8h)
- [ ] AP 4.5: Druckmodul entwickeln (5h)
- [ ] AP 4.6: Unit-Tests schreiben (8h)
- [ ] AP 4.7: Integrationstests (4h)
- [ ] AP 4.8: Gate 4 Review (1h)

**Gesamt Phase 4:** ca. 53h (größter Block!)

### Phase 5: V&V
- [ ] AP 5.1: Test Cases abarbeiten (10h)
- [ ] AP 5.2: E2E-Tests durchführen (5h)
- [ ] AP 5.3: Bug-Fixing (8h)
- [ ] AP 5.4: Regression-Tests (3h)
- [ ] AP 5.5: Performance-Tests (2h)
- [ ] AP 5.6: Test-Report erstellen (2h)
- [ ] AP 5.7: Gate 5 Review (1h)

**Gesamt Phase 5:** ca. 31h

### Phase 6: Beta
- [ ] AP 6.1: Beta-Version verteilen (1h)
- [ ] AP 6.2: Feedback sammeln (wöchentlich, 3 Wochen) (6h)
- [ ] AP 6.3: Usability-Anpassungen (5h)
- [ ] AP 6.4: Dokumentation finalisieren (3h)
- [ ] AP 6.5: Gate 6 Review (1h)

**Gesamt Phase 6:** ca. 16h

### Phase 7: Release
- [ ] AP 7.1: Finale Version bauen (1h)
- [ ] AP 7.2: Release Notes schreiben (1h)
- [ ] AP 7.3: Download-Seite / App-Store (2h)
- [ ] AP 7.4: Marketing (optional) (2h)
- [ ] AP 7.5: Gate 7 Review (1h)

**Gesamt Phase 7:** ca. 7h

---

**Gesamtaufwand (geschätzt):** ca. 172h  
**Bei 10h/Woche:** ca. 17 Wochen = **4 Monate**  
**Bei 15h/Woche:** ca. 11 Wochen = **2.5-3 Monate**

---

## 6. Ressourcenplanung

### 6.1 Personelle Ressourcen

| Rolle | Person/Tool | Verfügbarkeit | Verantwortung |
|-------|-------------|---------------|---------------|
| Projektleiter | Du | 10-15h/Woche | Gesamtverantwortung, Entscheidungen |
| Anforderungsanalyst | Du + Claude | Nach Bedarf | Requirements erfassen & dokumentieren |
| Software-Architekt | Du + Claude | Phase 2-3 | Architektur & Konzept |
| Entwickler | Du + Claude Code | Phase 4-5 | Implementierung |
| Tester | Du | Phase 5-6 | V&V, Beta-Testing |
| Dokumentation | Claude | Alle Phasen | Technische Dokumentation |
| Beta-Tester | 2-3 Imkerkollegen | Phase 6 (3 Wochen) | Feedback, Feldtest |

### 6.2 Zeitliche Ressourcen

**Verfügbare Arbeitszeit:**

- **Wochentage:** ca. 2h/Abend = 10h/Woche
- **Wochenende:** ca. 5h = zusätzlich verfügbar
- **Gesamt:** 10-15h/Woche planbar

**Urlaubsplanung / Blockaden:**

- [Hier eintragen wenn bekannt, z.B. Sommerurlaub]
- Bienensaison (April-August): Weniger Zeit verfügbar
- Winter (November-Februar): Mehr Zeit verfügbar

### 6.3 Finanzielle Ressourcen (Budget)

| Position | Kosten | Anmerkung |
|----------|--------|-----------|
| Entwicklungstools | 0 € | VS Code, Git = kostenlos |
| Datenbank | 0 € | SQLite = kostenlos |
| Heim-Server | 0 € | Raspberry Pi 5 (vorhanden) |
| Hosting (optional) | 0 € | Selbst-gehostet auf Raspberry Pi |
| App-Store Google Play | 25 € einmalig | Optional - noch zu entscheiden |
| App-Store Apple | 99 €/Jahr | Optional - noch zu entscheiden |
| Domain (optional) | 10 €/Jahr | Falls Download-Website gewünscht |
| Testing-Gerät | 0 € | Eigenes Smartphone |
| **Gesamt (minimal)** | **0 €** | Nur lokale Nutzung, kein Store |
| **Gesamt (mit Google Play)** | **25 €** | Android App-Store |
| **Gesamt (maximal)** | **134 €** | Mit iOS, Google Play, Domain |

**Budget-Status:** ✅ Genehmigt (Eigenfinanzierung)

**Anmerkungen:**

- Raspberry Pi 5 hostet Heim-Datenbank (MySQL/PostgreSQL möglich)
- App-Store-Veröffentlichung wird in Phase 7 entschieden
- Alternative: Direkter APK-Download (keine Store-Gebühren)

### 6.4 Technische Ressourcen

**Hardware:**

- Entwicklungs-PC (vorhanden)
- Test-Smartphone Android (vorhanden)
- Optional: iOS-Testgerät (falls benötigt)
- Raspberry Pi 5 als Heim-Server (vorhanden)

**Software:**

- Siehe Kapitel 7 (Tool-Stack)

---


## 7. Tool-Stack

### 7.1 Entwicklungsumgebung

| Kategorie | Tool | Zweck | Kosten |
|-----------|------|-------|--------|
| **Code-Editor** | VS Code | Haupt-IDE | Kostenlos |
| **Versionsverwaltung** | Git + GitHub | Code-Versionierung | Kostenlos |
| **Markdown-Editor** | VS Code / Notepad++ | Dokumentation | Kostenlos |
| **Diagramme** | Mermaid.live / draw.io | Architektur-Diagramme | Kostenlos |
| **Projektmanagement** | Markdown-Dateien + Git | Planung, Tracking | Kostenlos |

### 7.2 App-Entwicklung

**Technologie-Entscheidung:** (wird in Phase 2 finalisiert)

| Option | Pro | Contra | Status |
|--------|-----|--------|--------|
| **Flutter** | Cross-Platform, schnell, modern | Dart lernen | ⬜ Zu prüfen |
| **React Native** | JavaScript, große Community | Performance | ⬜ Zu prüfen |
| **PWA (Progressive Web App)** | Kein App-Store nötig, einfach | Offline-DB komplexer | ⬜ Zu prüfen |
| **Native Android (Kotlin)** | Beste Performance | Nur Android, mehr Aufwand | ⬜ Zu prüfen |

**Empfehlung:** Wird in `docs/06_konzept/technologie_entscheidung.md` dokumentiert

### 7.3 Datenbank

| Komponente | Tool | Begründung |
|------------|------|------------|
| **Lokale DB (App)** | SQLite | Standard für Mobile, offline-fähig |
| **Heim-DB** | SQLite oder PostgreSQL | SQLite: einfach / PostgreSQL: robuster für Raspberry Pi |
| **DB-Management** | DB Browser for SQLite / pgAdmin | Kostenlos, einfach zu bedienen |
| **Heim-Server** | Raspberry Pi 5 | Vorhanden, ausreichend Performance |

### 7.4 Synchronisation

| Option | Tool/Methode | Status |
|--------|--------------|--------|
| **WLAN-Transfer** | Custom REST API (auf Raspberry Pi) | ⬜ Zu implementieren |
| **USB-Transfer** | File-Export/Import (JSON/CSV) | ⬜ Fallback-Option |
| **Cloud-Sync** | Optional (Nextcloud auf Raspberry Pi) | ⬜ Version 2.0 |

### 7.5 Dokumentation & Kommunikation

| Zweck | Tool |
|-------|------|
| Technische Doku | Markdown + Git |
| Diagramme | Mermaid, draw.io |
| Konvertierung MD→Word | Pandoc |
| KI-Unterstützung | Claude AI, Claude Code |
| Beta-Feedback | Google Forms / Typeform |

### 7.6 Testing

| Test-Art | Tool |
|----------|------|
| Unit-Tests | Framework abhängig (Jest, Flutter Test) |
| Integrationstests | Manuell + Test-Scripts |
| E2E-Tests | Manuell nach Testplan |
| Performance | Chrome DevTools / Android Profiler |

---

## 8. Risikomanagement (Übersicht)

**Hinweis:** Detaillierte Risikoanalyse siehe `docs/04_risikoanalyse.md`

### 8.1 Top 5 Risiken

| ID | Risiko | Wahrscheinlichkeit | Auswirkung | Maßnahme |
|----|--------|-------------------|------------|----------|
| R1 | Unklare Behördenanforderungen | Mittel | Hoch | Früh mit Veterinäramt klären (Phase 1) |
| R2 | Datenverlust bei Sync | Niedrig | Sehr hoch | Backup-Strategie, Transaktionssicherheit |
| R3 | Technologie-Wahl falsch | Mittel | Hoch | Prototyp in Phase 2, früh testen |
| R4 | Zeitüberschreitung | Mittel | Mittel | MVP-Fokus, Nice-to-Haves streichen |
| R5 | Keine Beta-Tester | Niedrig | Mittel | Früh im Imkerverein anfragen |

### 8.2 Risiko-Monitoring

**Wann:** Jede Woche im Status-Check

**Vorgehen:**

1. Risiko-Liste durchgehen
2. Status aktualisieren (Wahrscheinlichkeit/Auswirkung)
3. Neue Risiken aufnehmen
4. Maßnahmen tracken

**Dokumentation:** `docs/04_risikoanalyse.md` (wird laufend aktualisiert)

---


## 9. Change Management

### 9.1 Change Request Prozess

Wann wird ein Change Request (CR) erstellt?

Neue Requirements entdeckt
Bestehende Requirements ändern sich
Technologie-Wechsel nötig
Scope-Änderung gewünscht

### 9.2 CR-Workflow

Change identifiziert
CR dokumentieren (siehe Template unten)
Impact-Analyse (Zeit, Kosten, Risiko)
Entscheidung: Akzeptieren / Ablehnen / Verschieben
Falls akzeptiert:
Projektplan anpassen
Betroffene Dokumente updaten
Phase-Rücksprung falls nötig
CR-Status auf "Umgesetzt" setzen

### 9.3 Change Request Template

In docs/change_requests.md dokumentieren:

Format:

unknown
Copy
## CR-001: [Kurztitel]
**Datum:** YYYY-MM-DD
**Status:** Offen / Akzeptiert / Umgesetzt / Abgelehnt
**Priorität:** Hoch / Mittel / Niedrig

**Beschreibung:**
[Was soll geändert werden?]

**Begründung:**
[Warum ist die Änderung nötig?]

**Impact-Analyse:**
- Betroffene Phasen: [z.B. Phase 2, 3]
- Zeitaufwand: [z.B. +5h]
- Risiko: [Hoch/Mittel/Niedrig]

**Entscheidung:**
- [ ] Akzeptiert
- [ ] Abgelehnt (Begründung: ...)
- [ ] Verschoben auf Version 2.0

**Maßnahmen:**
- [ ] Requirements anpassen
- [ ] Architektur überarbeiten
- [ ] Tests ergänzen

### 9.4 Priorisierung von Changes

**Kriterien:**

1. Kritisch: Behördenanforderungen, Datenverlust-Risiko → Sofort umsetzen
2. Hoch: Funktionale Must-Haves → In aktuelle Phase integrieren
3. Mittel: Nice-to-Haves → Evaluieren (evtl. v2.0)
4. Niedrig: Kosmetik, Extras → Version 2.0


---
## 10. Qualitätssicherung

### 10.1 Qualitätsziele

| Kriterium | Zielwert | Messung |
|-----------|----------|---------|
| **Funktionalität** | 100% Must-Haves implementiert | REQ-Traceability-Matrix |
| **Zuverlässigkeit** | Keine Datenverluste | Sync-Tests, Backup-Tests |
| **Benutzerfreundlichkeit** | Beta-Bewertung ≥ 4/5 | Feedback-Fragebogen |
| **Performance** | App-Start < 2 Sek. | Performance-Tests |
| **Wartbarkeit** | Code-Dokumentation 100% | Code-Review |
| **Testabdeckung** | Unit-Tests > 80% | Test-Coverage-Tool |

### 10.2 Review-Prozesse

#### Gate-Reviews (nach jeder Phase)

**Teilnehmer:** Projektleiter (du) + optional Claude AI

**Ablauf:**

1. **Vorbereitung:** Alle Deliverables bereitstellen
2. **Review-Meeting:** Checkliste durchgehen
3. **Entscheidung:** Go / No-Go / Rework
4. **Dokumentation:** Ergebnis in Projektplan eintragen

**Gate-Checkliste:** Siehe Kapitel 3.2 (Exit-Kriterien pro Phase)

#### Code-Reviews (Phase 4)

**Wann:** Vor jedem Git-Commit größerer Features

**Checkliste:**

- [ ] Code ist kommentiert (komplexe Stellen)
- [ ] Keine Hard-Coded Werte (Config-Files nutzen)
- [ ] Error-Handling vorhanden
- [ ] Unit-Tests geschrieben
- [ ] Code läuft ohne Warnungen

#### Dokumentations-Reviews

**Wann:** Nach jeder Phase

**Prüfung:**

- [ ] Alle Dokumente vollständig
- [ ] Versionsnummer aktualisiert
- [ ] Änderungshistorie gepflegt
- [ ] Verlinkungen funktionieren

### 10.3 Testing-Strategie

**Siehe detailliert:** `docs/08_testing/testplan.md`

**Übersicht:**

| Test-Typ | Wann | Verantwortlich | Tool |
|----------|------|----------------|------|
| Unit-Tests | Phase 4 (laufend) | Entwickler | Framework-abhängig |
| Integrationstests | Phase 4 (nach Features) | Entwickler | Custom Scripts |
| Systemtests | Phase 5 | Tester | Manuell nach Testplan |
| Regressionstests | Nach Bugfixes | Tester | Wiederholung kritischer Tests |
| Akzeptanztests | Phase 5 | Projektleiter | Testcases gegen REQs |
| Beta-Tests | Phase 6 | Beta-Nutzer | Reale Nutzung |

### 10.4 Definition of Done (DoD)

**Eine Phase gilt als "Done" wenn:**

- ✅ Alle Deliverables erstellt
- ✅ Gate-Exit-Kriterien erfüllt
- ✅ Dokumentation aktualisiert
- ✅ Tests bestanden (falls Phase 4+)
- ✅ Gate-Review durchgeführt & Go-Entscheidung
- ✅ Git-Commit mit Phase-Tag (z.B. `git tag phase-2-complete`)

**Ein Feature gilt als "Done" wenn:**

- ✅ Code implementiert
- ✅ Unit-Tests geschrieben & bestanden
- ✅ Code-Review durchgeführt
- ✅ Dokumentiert (Code-Kommentare + Doku-Update)
- ✅ In Testumgebung deployed & getestet

---

## 11. Zeitplanung (Timeline)

### 11.1 Meilenstein-Gantt (Übersicht)

| Phase | Meilenstein | KW | Apr | Mai | Jun | Jul |
|-------|-------------|----|----|-----|-----|-----|
| 0 | M0: Kickoff | 13 | ✅ | | | |
| 0 | M1: Projektplan fertig | 14 | 🚧 | | | |
| 1 | M2: REQs finalisiert | 15-16 | ███ | | | |
| 2 | M3: Konzept abgenommen | 17-18 | | ███ | | |
| 3 | M4: Detaildesign review | 19-20 | | ███ | | |
| 4 | M5: Prototyp läuft | 21-24 | | ███ | ███ | |
| 5 | M6: V&V abgeschlossen | 24-25 | | | ███ | |
| 6 | M7: Beta abgeschlossen | 26-27 | | | | ███ |
| 7 | M8: Release v1.0 | 27 | | | | ✅ |

**Legende:**  
✅ = Abgeschlossen  
🚧 = In Arbeit  
███ = Geplante Bearbeitungszeit  

### 11.2 Detaillierte Zeitplanung

| Phase | Start (KW) | Ende (KW) | Dauer | Aufwand (h) |
|-------|-----------|----------|-------|-------------|
| Phase 0: Planung | KW 13 | KW 14 | 1-2 Wochen | 12h |
| Phase 1: Requirements | KW 15 | KW 16 | 2 Wochen | 15h |
| Phase 2: Konzept | KW 17 | KW 18 | 2 Wochen | 20h |
| Phase 3: Detaildesign | KW 19 | KW 20 | 2 Wochen | 18h |
| Phase 4: Implementation | KW 21 | KW 24 | 4 Wochen | 53h |
| Phase 5: V&V | KW 24 | KW 25 | 2 Wochen | 31h |
| Phase 6: Beta | KW 26 | KW 27 | 2 Wochen | 16h |
| Phase 7: Release | KW 27 | KW 27 | 1 Woche | 7h |
| **Gesamt** | **KW 13** | **KW 27** | **ca. 15 Wochen** | **172h** |

**Bei 10h/Woche:** ca. 17 Wochen (4 Monate)  
**Bei 15h/Woche:** ca. 11 Wochen (2.5-3 Monate)

### 11.3 Kritischer Pfad

**Sequenzielle Abhängigkeiten (können nicht parallel laufen):**

Phase 0 → Phase 1 → Phase 2 → Phase 3 → Phase 4 → Phase 5 → Phase 6 → Phase 7


**Parallele Aktivitäten (während aller Phasen):**

- Dokumentation aktualisieren
- Risiko-Monitoring
- Change-Requests bearbeiten

**Puffer:** 

- Zwischen Phase 4-5: +1 Woche Puffer (falls Implementierung länger dauert)
- Zwischen Phase 5-6: +1 Woche Puffer (falls viele Bugs)

**Worst Case:** +4 Wochen Verzögerung = 19 Wochen gesamt

---

## 12. Entscheidungslog

**Hinweis:** Wird laufend gefüllt. Wichtige Projektentscheidungen hier dokumentieren.

### Format:

Entscheidung E-001: [Titel]
Datum: YYYY-MM-DD Entscheider: [Name] Status: Entschieden / Offen / Revidiert

Kontext: [Warum musste entschieden werden?]

Optionen:

Option A: [Beschreibung] - Pro: ... / Contra: ...
Option B: [Beschreibung] - Pro: ... / Contra: ...
Entscheidung: → Gewählt: Option X

Begründung: [Warum diese Option?]

Auswirkungen:

[z.B. Zeitplan, Budget, Risiken]
Review-Datum: [Optional: Wann wird Entscheidung überprüft?]

### Beispiel-Einträge:

#### E-001: Projektsteckbrief genehmigt

**Datum:** 2024-03-28  
**Entscheider:** Projektleiter  
**Status:** ✅ Entschieden

**Entscheidung:** Projektsteckbrief Version 1.0 freigegeben, Projekt startet.

**Begründung:** Ziele klar, Ressourcen verfügbar, Motivation hoch.

---

#### E-002: Markdown als Dokumentationsformat

**Datum:** 2024-03-28  
**Entscheider:** Projektleiter  
**Status:** ✅ Entschieden

**Kontext:** Dokumentation muss versionierbar, KI-lesbar und Word-kompatibel sein.

**Optionen:**

1. Word (.docx) - Pro: Gewohnt / Contra: Nicht Git-freundlich
2. Markdown (.md) - Pro: Git, KI, Pandoc → Word / Contra: Weniger Formatierung

**Entscheidung:** → Markdown als Master-Format

**Begründung:** 

- Git-Versionierung wichtig
- Claude/Claude Code können MD direkt lesen
- Pandoc konvertiert bei Bedarf zu Word

**Auswirkungen:** Pandoc muss installiert werden (erledigt)

---

#### E-003: Technologie-Stack für App

**Datum:** TBD (Phase 2)  
**Status:** ⬜ Offen

**Optionen:**

1. Flutter
2. React Native
3. PWA
4. Native Android (Kotlin)

**Entscheidung:** Wird in Phase 2 nach Prototyping getroffen.

**Kriterien:**

- Offline-Fähigkeit
- Entwicklungsgeschwindigkeit
- Lernkurve
- Zukunftssicherheit

---

*(Weitere Entscheidungen werden hier ergänzt)*

---