# Requirements: Bienenapp (BSK-App)

**Projekt:** Bienenapp - Digitale Stockkartenverwaltung  
**Dokument:** Funktionale Requirements (aus Stakeholder-Analyse)  
**Version:** 0.1  
**Datum:** 2024-03-28  
**Status:** Initial Draft  

---

## 1. Stakeholder-Requirements

### REQ-S1: Anforderungen Projektleiter (Hauptnutzer)

**REQ-S1.1: Offline-Funktionalität**

- **Quelle:** Stakeholder S1 (Du)
- **Beschreibung:** App muss vollständig offline im Bienenstand nutzbar sein (keine Internetverbindung erforderlich)
- **Begründung:** Bienenstände haben oft kein Mobilfunknetz
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** Alle Funktionen (Eingabe, Anzeige, Suche) funktionieren ohne Internet

---

**REQ-S1.2: Keine Datenverluste**

- **Quelle:** Stakeholder S1 (Du)
- **Beschreibung:** Daten dürfen bei Synchronisation oder App-Absturz nicht verloren gehen
- **Begründung:** Stockkarten sind rechtlich relevante Dokumente
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** 
  - Lokale Daten bleiben erhalten bis erfolgreicher Sync
  - Automatisches Backup vorhanden
  - Wiederherstellung möglich

---

**REQ-S1.3: Einfache Bedienung**

- **Quelle:** Stakeholder S1 (Du)
- **Beschreibung:** App muss intuitiv bedienbar sein, auch mit Handschuhen im Bienenstand
- **Begründung:** Schnelle Eingabe vor Ort wichtig
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** 
  - Große Buttons (min. 44x44px)
  - Eingabe max. 5 Schritte
  - Beta-Tester bewerten Usability ≥ 4/5

---

**REQ-S1.4: Projektzeitrahmen**

- **Quelle:** Stakeholder S1 (Du)
- **Beschreibung:** MVP (Minimum Viable Product) in max. 3 Monaten fertig
- **Begründung:** Motivation und Verfügbarkeit
- **Priorität:** Should-Have
- **Akzeptanzkriterium:** Release bis KW 27 (Ende Juni)

---

### REQ-S2: Anforderungen Veterinäramt

**REQ-S2.1: Vollständige Dokumentation**

- **Quelle:** Stakeholder S2 (Veterinäramt)
- **Beschreibung:** Alle behördlich vorgeschriebenen Pflichtfelder müssen erfasst werden
- **Begründung:** Einhaltung Bienenseuchenverordnung
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** 
  - Alle Felder gemäß Verordnung vorhanden (wird in Phase 1 detailliert)
  - Pflichtfelder erzwingen Eingabe

---

**REQ-S2.2: Papierausdruck verfügbar**

- **Quelle:** Stakeholder S2 (Veterinäramt)
- **Beschreibung:** Stockkarten müssen als PDF gedruckt werden können
- **Begründung:** Bei Kontrollen werden ausgedruckte Stockkarten verlangt
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** 
  - PDF-Export aus Heim-DB
  - Format entspricht offizieller Stockkarte
  - Lesbar, strukturiert, vollständig

---

**REQ-S2.3: Nachvollziehbare Dokumentation**

- **Quelle:** Stakeholder S2 (Veterinäramt)
- **Beschreibung:** Einträge müssen datiert und chronologisch sein
- **Begründung:** Rückverfolgbarkeit bei Seuchenausbruch
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** 
  - Jeder Eintrag hat Timestamp
  - Sortierung nach Datum möglich
  - Keine nachträgliche Änderung ohne Hinweis

---

### REQ-S3: Anforderungen Beta-Tester

**REQ-S3.1: Intuitive Bedienung**

- **Quelle:** Stakeholder S3 (Imkerkollegen)
- **Beschreibung:** App muss ohne Anleitung verständlich sein
- **Begründung:** Nutzer haben keine Zeit für lange Einarbeitung
- **Priorität:** Should-Have
- **Akzeptanzkriterium:** 
  - Neue Nutzer können innerhalb 5 Minuten ersten Eintrag erstellen
  - Beta-Feedback: "Bedienung klar"

---

**REQ-S3.2: Stabiler Betrieb**

- **Quelle:** Stakeholder S3 (Imkerkollegen)
- **Beschreibung:** App darf nicht abstürzen oder hängen bleiben
- **Begründung:** Vertrauensverlust bei Fehlern
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** 
  - Keine Abstürze in Beta-Phase
  - Error-Handling für alle kritischen Funktionen

---

**REQ-S3.3: Einfache Installation**

- **Quelle:** Stakeholder S3 (Imkerkollegen)
- **Beschreibung:** Installation per APK-Download (kein kompliziertes Setup)
- **Begründung:** Niedrige Einstiegshürde für Beta-Tester
- **Priorität:** Should-Have
- **Akzeptanzkriterium:** 
  - APK-Link zum Download
  - Installation in max. 2 Klicks

---

### REQ-S4: Anforderungen Imkerverein

**REQ-S4.1: Mehrfachnutzung möglich**

- **Quelle:** Stakeholder S4 (Imkerverein)
- **Beschreibung:** Andere Imker sollen die App ebenfalls nutzen können
- **Begründung:** Community-Tool, nicht nur für einen Nutzer
- **Priorität:** Could-Have (Version 2.0)
- **Akzeptanzkriterium:** 
  - Download-Link verfügbar
  - Anleitung vorhanden

---

### REQ-S5: Anforderungen Claude AI / Claude Code

**REQ-S5.1: Klare Dokumentation**

- **Quelle:** Stakeholder S5 (Claude AI)
- **Beschreibung:** Requirements und Architektur müssen strukturiert dokumentiert sein
- **Begründung:** KI benötigt Kontext zum Helfen
- **Priorität:** Must-Have
- **Akzeptanzkriterium:** 
  - Alle REQs in Markdown
  - Architektur-Diagramm vorhanden
  - Code-Kommentare vorhanden

---

### REQ-S6: Anforderungen Familie/Freunde

**REQ-S6.1: Realistischer Zeitaufwand**

- **Quelle:** Stakeholder S6 (Familie)
- **Beschreibung:** Projekt darf Freizeit nicht komplett blockieren
- **Begründung:** Work-Life-Balance
- **Priorität:** Should-Have
- **Akzeptanzkriterium:** 
  - Max. 15h/Woche
  - Flexible Planung bei Verzögerungen

---

## 2. Zusammenfassung: Must-Have Requirements

| REQ-ID | Beschreibung | Stakeholder |
|--------|--------------|-------------|
| REQ-S1.1 | Offline-Funktionalität | Du |
| REQ-S1.2 | Keine Datenverluste | Du |
| REQ-S1.3 | Einfache Bedienung | Du |
| REQ-S2.1 | Vollständige Dokumentation (Pflichtfelder) | Veterinäramt |
| REQ-S2.2 | Papierausdruck (PDF) | Veterinäramt |
| REQ-S2.3 | Nachvollziehbare Dokumentation | Veterinäramt |
| REQ-S3.2 | Stabiler Betrieb | Beta-Tester |
| REQ-S5.1 | Klare Dokumentation | Claude AI |

---

## 3. Nächste Schritte (Phase 1)

- [ ] Veterinäramt kontaktieren → Pflichtfelder klären
- [ ] Bienenseuchenverordnung recherchieren
- [ ] Funktionale Requirements detaillieren
- [ ] Nicht-funktionale Requirements ergänzen
- [ ] Traceability-Matrix anlegen

---

## 4. Änderungshistorie

| Version | Datum | Änderung |
|---------|-------|----------|
| 0.1 | 2024-03-28 | Initiale Erstellung aus Stakeholder-Analyse |

---
