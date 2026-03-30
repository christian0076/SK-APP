# Risikoanalyse: Bienenapp (BSK-App)

**Projekt:** Bienenapp - Digitale Stockkartenverwaltung  
**Dokument:** Detaillierte Risikoanalyse  
**Version:** 1.0  
**Datum:** 2024-03-28  
**Status:** In Arbeit  

---

## 1. Übersicht

Dieses Dokument beschreibt alle identifizierten Projektrisiken, deren Bewertung und Gegenmaßnahmen.

**Risiko-Bewertung:**

- **Wahrscheinlichkeit:** Niedrig / Mittel / Hoch
- **Auswirkung:** Niedrig / Mittel / Hoch / Sehr hoch
- **Risiko-Score:** Wahrscheinlichkeit × Auswirkung

**Risiko-Kategorien:**

| Score | Kategorie | Aktion |
|-------|-----------|--------|
| Niedrig × Niedrig | Grün | Beobachten |
| Mittel × Mittel | Gelb | Maßnahmen planen |
| Hoch × Hoch | Rot | Sofort handeln |

---

## 2. Risiko-Register

### R1: Unklare Behördenanforderungen

**Kategorie:** Requirements  
**Wahrscheinlichkeit:** Mittel  
**Auswirkung:** Hoch  
**Risiko-Score:** 🟡 Gelb  

**Beschreibung:**

Veterinäramt-Anforderungen und Bienenverordnungen sind nicht vollständig dokumentiert oder ändern sich.

**Auswirkungen:**

- Stockkarten entsprechen nicht den Vorgaben
- App wird von Behörden nicht akzeptiert
- Nachträgliche Änderungen → Phase-Rücksprung → Zeitverzögerung

**Gegenmaßnahmen:**

1. **Proaktiv (Phase 1):**
   - Frühzeitig Kontakt zum Veterinäramt aufnehmen
   - Offizielle Verordnungen recherchieren (Bienenseuchenverordnung, etc.)
   - Stockkarten-Muster vom Veterinäramt anfordern
   - Requirements schriftlich dokumentieren & bestätigen lassen

2. **Reaktiv:**
   - Flexibles Design: Stockkarten-Template anpassbar
   - Change-Request-Prozess für REQ-Änderungen

**Verantwortlich:** Projektleiter  
**Status:** ⬜ Offen (wird in Phase 1 adressiert)  
**Review-Datum:** KW 16 (Ende Phase 1)

---

### R2: Datenverlust bei Synchronisation

**Kategorie:** Technisch  
**Wahrscheinlichkeit:** Niedrig  
**Auswirkung:** Sehr hoch  
**Risiko-Score:** 🟡 Gelb  

**Beschreibung:**

Daten gehen bei der Synchronisation zwischen App und Heim-DB verloren (z.B. Netzwerkabbruch, Fehler im Sync-Code).

**Auswirkungen:**

- Stockkarten-Einträge unwiederbringlich verloren
- Vertrauensverlust bei Nutzern
- Behördliche Probleme bei fehlender Dokumentation

**Gegenmaßnahmen:**

1. **Technisch:**
   - **Transaktionssicherheit:** Nur vollständige Sync-Vorgänge committen
   - **Lokales Backup:** App behält Daten bis erfolgreicher Sync bestätigt
   - **Versionierung:** Timestamps für jede Änderung
   - **Konfliktauflösung:** Bei Sync-Konflikt manuelle Auswahl ermöglichen

2. **Prozess:**
   - **Automatisches Backup:** Heim-DB täglich auf Raspberry Pi sichern
   - **Export-Funktion:** Manuelle CSV/JSON-Exporte jederzeit möglich
   - **Integrationstests:** Sync-Szenarien ausgiebig testen (Abbruch, Offline, etc.)

3. **Dokumentation:**
   - Sync-Konzept in `docs/07_detaildesign/sync_konzept.md` detailliert beschreiben

**Verantwortlich:** Entwickler  
**Status:** ⬜ Offen (Konzept in Phase 3, Implementierung Phase 4)  
**Review-Datum:** KW 24 (Ende Phase 4)

---

### R3: Falsche Technologie-Wahl

**Kategorie:** Technisch  
**Wahrscheinlichkeit:** Mittel  
**Auswirkung:** Hoch  
**Risiko-Score:** 🟡 Gelb  

**Beschreibung:**

Gewähltes App-Framework (Flutter/React Native/PWA/Kotlin) erfüllt Requirements nicht (z.B. Offline-DB zu komplex, Performance zu schlecht).

**Auswirkungen:**

- Projekt-Neustart mit anderer Technologie → Zeitverlust 2-4 Wochen
- Frustration, Motivation sinkt
- Eventuell MVP-Features streichen

**Gegenmaßnahmen:**

1. **Proaktiv (Phase 2):**
   - **Prototyping:** Kleine Test-Apps mit verschiedenen Frameworks
   - **Bewertungskriterien festlegen:**
     - Offline-Fähigkeit (SQLite-Anbindung)
     - Entwicklungsgeschwindigkeit
     - Lernkurve (Vorwissen vorhanden?)
     - Community-Support
   - **Entscheidungsmatrix** in `docs/06_konzept/technologie_entscheidung.md`

2. **Reaktiv:**
   - Early Exit: Bei ersten Anzeichen von Problemen frühzeitig wechseln (lieber in Phase 2 als Phase 4)

**Verantwortlich:** Software-Architekt + Entwickler  
**Status:** ⬜ Offen (Entscheidung in Phase 2)  
**Review-Datum:** KW 18 (Ende Phase 2)

---

### R4: Zeitüberschreitung (Projekt dauert länger als 3 Monate)

**Kategorie:** Planung  
**Wahrscheinlichkeit:** Mittel  
**Auswirkung:** Mittel  
**Risiko-Score:** 🟡 Gelb  

**Beschreibung:**

Projekt dauert länger als geplant (>3 Monate) wegen:
- Unvorhergesehenen technischen Problemen
- Weniger verfügbare Zeit (Bienensaison, privat)
- Scope Creep (zu viele Features)

**Auswirkungen:**

- Motivation sinkt bei langer Dauer
- Saisonstart (April) verpasst für Beta-Test
- Andere Projekte werden blockiert

**Gegenmaßnahmen:**

1. **Proaktiv:**
   - **MVP-Fokus:** Nur Must-Have Features im ersten Release
   - **MoSCoW-Priorisierung:** Nice-to-Haves in v2.0 verschieben
   - **Puffer einplanen:** +4 Wochen Reserve im Zeitplan
   - **Wöchentliches Tracking:** Status-Check jeden Sonntag

2. **Reaktiv:**
   - **Features streichen:** Falls Verzögerung droht, reduzieren auf Minimum
   - **Hilfe holen:** Claude Code intensiver nutzen in Phase 4

**Verantwortlich:** Projektleiter  
**Status:** 🚧 Aktiv überwacht  
**Review-Datum:** Wöchentlich

---

### R5: Keine Beta-Tester verfügbar

**Kategorie:** Organisatorisch  
**Wahrscheinlichkeit:** Niedrig  
**Auswirkung:** Mittel  
**Risiko-Score:** 🟢 Grün  

**Beschreibung:**

Keine Imkerkollegen haben Zeit/Lust für Beta-Testing in Phase 6.

**Auswirkungen:**

- Keine realen Nutzungsdaten
- Usability-Probleme werden nicht entdeckt
- Beta-Phase verkürzt → direkt Release (riskanter)

**Gegenmaßnahmen:**

1. **Proaktiv:**
   - **Früh anfragen:** Bereits in Phase 1 Kollegen im Imkerverein ansprechen
   - **Incentive bieten:** Kostenlose App-Nutzung, Dankeschön (Honig?)
   - **Niedrige Hürde:** Beta muss super einfach installierbar sein (APK-Link)

2. **Reaktiv:**
   - **Selbst testen:** Mit eigenen Völkern ausgiebig testen (verlängerte Phase 5)
   - **Online-Community:** In Imker-Foren nach Beta-Testern suchen

**Verantwortlich:** Projektleiter  
**Status:** ⬜ Offen (Anfrage in Phase 1)  
**Review-Datum:** KW 16

---

### R6: Raspberry Pi fällt aus / ist nicht erreichbar

**Kategorie:** Technisch  
**Wahrscheinlichkeit:** Niedrig  
**Auswirkung:** Mittel  
**Risiko-Score:** 🟢 Grün  

**Beschreibung:**

Raspberry Pi 5 (Heim-Server) hat Hardware-Problem, SD-Karte defekt, oder Netzwerk nicht erreichbar.

**Auswirkungen:**

- Sync funktioniert nicht
- Daten nur lokal auf Smartphone
- Drucken nicht möglich

**Gegenmaßnahmen:**

1. **Proaktiv:**
   - **Backup der Heim-DB:** Automatisch täglich auf NAS sichern
   - **Hochwertige SD-Karte:** Industrial-Grade für Raspberry Pi
   - **Monitoring:** Einfacher Health-Check (Ping-Script)

2. **Reaktiv:**
   - **Fallback-Modus:** App funktioniert autark (nur Drucken nicht möglich)
   - **Export-Funktion:** Daten als CSV exportieren → auf anderem PC drucken
   - **Ersatz-Pi:** Notfall-Image bereithalten (schnelles Restore)

**Verantwortlich:** Projektleiter  
**Status:** ⬜ Offen (Backup-Strategie in Phase 4)  
**Review-Datum:** KW 24

---

### R7: Smartphone geht kaputt / verloren

**Kategorie:** Technisch  
**Wahrscheinlichkeit:** Niedrig  
**Auswirkung:** Hoch  
**Risiko-Score:** 🟡 Gelb  

**Beschreibung:**

Test-Smartphone geht kaputt, verloren oder wird gestohlen während Entwicklung/Nutzung.

**Auswirkungen:**

- Lokale Daten verloren (falls nicht synchronisiert)
- Entwicklung blockiert (kein Testgerät)

**Gegenmaßnahmen:**

1. **Proaktiv:**
   - **Regelmäßiger Sync:** Mindestens täglich Daten auf Heim-DB sichern
   - **Backup-Gerät:** Altes Smartphone als Notfall-Gerät bereithalten
   - **Cloud-Backup (optional):** Verschlüsseltes Backup auf Nextcloud (Raspberry Pi)

2. **Reaktiv:**
   - **App neu installieren:** Daten aus Heim-DB wiederherstellen
   - **Entwicklung:** Emulator nutzen (Android Studio / Xcode)

**Verantwortlich:** Projektleiter  
**Status:** 🟢 Akzeptiert (Wahrscheinlichkeit sehr niedrig)  
**Review-Datum:** -

---

## 3. Risiko-Matrix (Übersicht)

|               | **Niedrig** | **Mittel** | **Hoch** | **Sehr hoch** |
|---------------|-------------|------------|----------|---------------|
| **Hoch**      |             | R3         |          |               |
| **Mittel**    |             | R1, R4     |          |               |
| **Niedrig**   | R5, R6      | R7         | R2       |               |
|               | ↑ Auswirkung | → | → | → |
| **Wahrscheinlichkeit** → |

**Legende:**  
🔴 Rot = Kritisch (sofort handeln)  
🟡 Gelb = Überwachen (Maßnahmen geplant)  
🟢 Grün = Akzeptabel (beobachten)

---

## 4. Neue Risiken (Template)

**Wenn neue Risiken identifiziert werden:**


RX: [Risiko-Titel]
Kategorie: [Requirements / Technisch / Organisatorisch / Extern]
Wahrscheinlichkeit: [Niedrig / Mittel / Hoch]
Auswirkung: [Niedrig / Mittel / Hoch / Sehr hoch]
Risiko-Score: [🟢 / 🟡 / 🔴]

Beschreibung: [Was ist das Risiko?]

Auswirkungen:

[Was passiert wenn es eintritt?]
Gegenmaßnahmen:

Proaktiv:

[Wie verhindern wir es?]
Reaktiv:

[Was tun wenn es eintritt?]
Verantwortlich: [Person]
Status: [⬜ Offen / 🚧 In Arbeit / ✅ Erledigt]
Review-Datum: [KW XX]



---

## 5. Risiko-Review-Termine

| Wann | Was |
|------|-----|
| **Wöchentlich** | Kurzer Check: Sind neue Risiken aufgetaucht? Status-Update |
| **Nach jedem Gate** | Vollständiger Review aller Risiken |
| **Bei Eintreten** | Sofortiges Krisenmeeting, Maßnahmen aktivieren |

**Nächster Review:** KW 14 (Ende Phase 0)

---

## 6. Änderungshistorie

| Version | Datum | Autor | Änderung |
|---------|-------|-------|----------|
| 1.0 | 2024-03-28 | Claude AI | Initiale Erstellung mit 7 Risiken |

---

**Freigabe:**

- [ ] Projektleiter: _________________ Datum: _______

