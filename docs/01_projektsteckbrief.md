# Projektsteckbrief: Bienenapp - Stockkarten App

**Projekt:** Bienenapp - Digitale Stockkartenverwaltung  
**Projektkürzel:** BSK-App  
**Version:** 1.0  
**Datum:** 2024-03-28  
**Status:** In Planung  

---

## 1. Projektübersicht

| Kategorie | Information |
|-----------|-------------|
| **Projektname** | Bienenapp - Digitale Stockkartenverwaltung |
| **Projektkürzel** | BSK-App |
| **Projektleitung** | [Dein Name einfügen] |
| **Projektunterstützung** | Claude AI (Planung, Konzept, Dokumentation) |
| **Projektstart** | [Datum einfügen] |
| **Geplantes Ende** | ca. 2-3 Monate (MVP) |
| **Status** | In Planung |

---

## 2. Projektziel

Entwicklung einer mobilen App zur digitalen Erfassung von Stockkarten für Bienenvölker mit folgenden Hauptfunktionen:

- **Offline-Nutzung** im Bienenstand
- **Datentransfer** in heimische Datenbank
- **Druckfunktion** für behördenkonforme Stockkarten
- **Einhaltung** veterinärrechtlicher Vorgaben

---

## 3. Projekthintergrund & Motivation

### Problem
- Papierstockkarten sind unpraktisch bei Feldarbeit
- Manuelle Übertragung fehleranfällig und zeitaufwendig
- Behörden verlangen vollständige, lesbare Dokumentation aller Völker

### Lösung
Digitale mobile Erfassung + zentrale Datenhaltung + Druck auf Abruf

---

## 4. Stakeholder

| Stakeholder | Rolle | Interesse/Anforderungen |
|-------------|-------|------------------------|
| Imker (Projektinhaber) | Hauptnutzer, Entwickler | Effizienz, Rechtssicherheit, Benutzerfreundlichkeit |
| Veterinäramt | Kontrollbehörde | Vollständige, korrekte Dokumentation gemäß Verordnung |
| Andere Imker | Potenzielle Nutzer (Beta/Kunden) | Einfache Bedienung, Zuverlässigkeit, Preis-Leistung |
| App-Stores | Vertriebsplattform | Qualitätsstandards, Richtlinien-Konformität |

---

## 5. Projektphasen (Übersicht)

1. **Planung** (inkl. Stakeholder-Analyse, Tool-Auswahl)
2. **Requirements Capture** (Veterinäramt, Verordnungen, eigene REQs)
3. **Konzept** (SW-Architektur, Mockups, Prototyping)
4. **Detaildesign** (Implementierung, DB-Design, Test Cases)
5. **Integration** (Deployment auf Testgerät, DB-Anbindung)
6. **Verification & Validation** (Systematisches Testen)
7. **Beta-Phase** (Feldtest mit echten Völkern)
8. **Release** (App-Store Upload / Download-Bereitstellung)
9. **Service & Wartung** (Support, Updates, Bugfixes)

**Parallel laufend:** Risk Management, Change Management

---

## 6. Hauptkomponenten (System-Übersicht)

- **Mobile App** (Android/iOS oder PWA)
- **Lokale Datenbank** (SQLite auf Handy)
- **Heimdatenbank** (PC/Server - MySQL/PostgreSQL/SQLite)
- **Sync-Mechanismus** (WLAN/USB/Cloud-basiert)
- **Druckmodul** (PDF-Generierung aus DB-Daten)

---

## 7. Erfolgskriterien

✅ App erfasst alle behördlich geforderten Daten korrekt  
✅ Offline-Betrieb funktioniert zuverlässig (keine Internetverbindung nötig)  
✅ Gedruckte Stockkarten entsprechen behördlichen Vorgaben  
✅ Datenverlust ausgeschlossen (Backup/Sync-Strategie)  
✅ Beta-Tester bewerten App mit mind. 4/5 Sternen  
✅ Sync zwischen App und Heim-DB funktioniert fehlerfrei  

---

## 8. Risiken (erste Übersicht)

| Risiko | Wahrscheinlichkeit | Auswirkung | Gegenmaßnahme |
|--------|-------------------|------------|---------------|
| Unklare behördliche Anforderungen | Mittel | Hoch | Frühe Klärung mit Veterinäramt, Verordnungen prüfen |
| Datenverlust bei Sync | Niedrig | Sehr hoch | Robuste Backup-Strategie, Transaktionssicherheit |
| Plattform-Kompatibilität | Mittel | Mittel | Plattformunabhängige Technologie (PWA) prüfen |
| Zeitüberschreitung | Mittel | Mittel | Agiles Vorgehen, MVP-Fokus |

*Detailliertes Risk Management in separatem Dokument*

---

## 9. Zeitschätzung (MVP)

| Phase | Aufwand (mit Claude-Unterstützung) | Meilenstein |
|-------|-----------------------------------|-------------|
| 1. Planung | 1 Woche | Projektplan & Tool-Auswahl abgeschlossen |
| 2. Requirements | 1-2 Wochen | REQ-Liste finalisiert & verifiziert |
| 3. Konzept | 1-2 Wochen | SW-Architektur & Mockups fertig |
| 4. Detaildesign | 3-5 Wochen | Lauffähiger Prototyp (App + DB) |
| 5. Integration | 1 Woche | App auf Testgerät deployed |
| 6. V&V | 2 Wochen | Alle Test Cases bestanden |
| 7. Beta | 2-3 Wochen | Feedback verarbeitet |
| 8. Release | 1 Woche | App verfügbar |
| **Gesamt** | **ca. 2-3 Monate** | **MVP produktiv** |

**Annahmen:**
- Verfügbare Zeit: 5-10h/Woche
- Technologie: PWA oder einfaches Framework (React Native/Flutter)
- Keine komplexen Sonderfunktionen im MVP

---

## 10. Budget & Ressourcen

| Position | Kosten/Aufwand |
|----------|----------------|
| Entwicklungszeit | Eigenleistung (siehe Zeitschätzung) |
| Tools & Software | Kostenlos (VS Code, Git, SQLite) oder minimal |
| Hosting (optional) | 0-10 €/Monat (falls Cloud-Sync gewünscht) |
| App-Store Gebühren | Google Play: 25 € einmalig / Apple: 99 €/Jahr |
| **Gesamt** | < 150 € (inkl. App-Store) |

---

## 11. Nächste Schritte

1. ✅ Projektsteckbrief finalisieren
2. ⬜ Projektplan erstellen (detailliert)
3. ⬜ Tool-Stack festlegen
4. ⬜ Requirements-Recherche starten (Veterinäramt kontaktieren)

---

## Änderungshistorie

| Version | Datum | Autor | Änderung |
|---------|-------|-------|----------|
| 1.0 | 2024-03-28 | Claude AI | Initiale Erstellung |

---

**Genehmigung:**

- [ ] Projektinhaber: _________________ Datum: _______

