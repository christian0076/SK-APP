# Change Requests: Bienenapp (BSK-App)

**Projekt:** Bienenapp - Digitale Stockkartenverwaltung  
**Dokument:** Change Request Tracking  
**Version:** 1.0  
**Datum:** 2024-03-28  
**Status:** Aktiv  

---

## 1. Übersicht

Dieses Dokument trackt alle Change Requests (Änderungsanfragen) während des Projekts.

**Zweck:**

- Strukturierte Erfassung von Änderungen
- Impact-Analyse vor Umsetzung
- Nachvollziehbarkeit von Entscheidungen
- Vermeidung von Scope Creep

**Status-Definitionen:**

- ⬜ **Offen:** Neu eingegangen, noch nicht bewertet
- 🔍 **In Prüfung:** Impact-Analyse läuft
- ✅ **Akzeptiert:** Wird umgesetzt
- 🚧 **In Umsetzung:** Wird gerade implementiert
- ✔️ **Umgesetzt:** Fertig, in Projekt integriert
- ❌ **Abgelehnt:** Wird nicht umgesetzt
- 📌 **Verschoben:** Auf Version 2.0 verschoben

---

## 2. Change Request Übersicht

| CR-ID | Titel | Datum | Status | Priorität | Phase |
|-------|-------|-------|--------|-----------|-------|
| CR-001 | *Beispiel: Zusätzliches Feld "Königin markiert"* | 2024-03-28 | ⬜ Offen | Niedrig | Phase 1 |

*(Tabelle wird laufend aktualisiert)*

---

## 3. Change Requests (Details)

### CR-001: [Beispiel - bitte löschen nach erstem echten CR]

**Datum:** 2024-03-28  
**Eingereicht von:** Projektleiter  
**Status:** ⬜ Offen  
**Priorität:** Niedrig  

**Beschreibung:**

Zusätzliches Feld in Stockkarte: "Königin markiert: Ja/Nein/Farbe"

**Begründung:**

Erleichtert Identifikation der Königin bei Durchsicht.

**Betroffene Bereiche:**

- Requirements (REQ_funktional.md)
- Datenmodell (Tabelle "Stockkarten")
- UI (Eingabemaske)
- Druckmodul (PDF-Template)

**Impact-Analyse:**

- **Zeit:** +2h (DB-Feld, UI-Element, Test)
- **Kosten:** 0 €
- **Risiko:** Niedrig
- **Betroffene Phasen:** Phase 3, 4

**Entscheidung:**

- [ ] ✅ Akzeptiert → Umsetzung in Phase X
- [ ] ❌ Abgelehnt → Begründung: ...
- [ ] 📌 Verschoben auf Version 2.0

**Begründung der Entscheidung:**

*[Wird nach Entscheidung ausgefüllt]*

**Maßnahmen bei Akzeptierung:**

- [ ] `REQ_funktional.md` aktualisieren
- [ ] Datenmodell erweitern
- [ ] UI anpassen
- [ ] Test Cases ergänzen
- [ ] Projektplan anpassen (falls Zeitverzögerung)

**Umgesetzt am:** -  
**Verifiziert am:** -

---

## 4. Template für neue Change Requests

**Bei neuem CR: Kopieren, ID hochzählen, ausfüllen**

---

### CR-XXX: [Kurztitel des Change Requests]

**Datum:** YYYY-MM-DD  
**Eingereicht von:** [Name / Rolle]  
**Status:** ⬜ Offen  
**Priorität:** [Kritisch / Hoch / Mittel / Niedrig]  

**Beschreibung:**

[Was soll geändert werden? Detaillierte Beschreibung]

**Begründung:**

[Warum ist die Änderung nötig? Welches Problem löst sie?]

**Betroffene Bereiche:**

- [z.B. Requirements, Architektur, Code, Tests, Dokumentation]

**Impact-Analyse:**

- **Zeit:** [Geschätzter Mehraufwand in Stunden]
- **Kosten:** [Falls zusätzliche Kosten entstehen]
- **Risiko:** [Niedrig / Mittel / Hoch]
- **Betroffene Phasen:** [z.B. Phase 2, 3, 4]
- **Abhängigkeiten:** [Andere CRs oder Features die betroffen sind]

**Entscheidung:**

- [ ] ✅ Akzeptiert → Umsetzung in Phase X
- [ ] ❌ Abgelehnt → Begründung: ...
- [ ] 📌 Verschoben auf Version 2.0

**Begründung der Entscheidung:**

*[Wird nach Entscheidung ausgefüllt]*

**Maßnahmen bei Akzeptierung:**

- [ ] [Konkrete Aufgabe 1]
- [ ] [Konkrete Aufgabe 2]
- [ ] [Projektplan anpassen falls nötig]

**Umgesetzt am:** -  
**Verifiziert am:** -

---

## 5. Priorisierungs-Matrix

**Entscheidungshilfe für Change Requests:**

| Priorität | Kriterien | Aktion |
|-----------|-----------|--------|
| **Kritisch** | Behördenanforderung, Datenverlust, Showstopper | Sofort umsetzen, notfalls Phase-Rücksprung |
| **Hoch** | Funktionale Must-Haves, Usability kritisch | In aktuelle Phase integrieren |
| **Mittel** | Nice-to-Haves, Verbesserungen | Evaluieren: Jetzt oder v2.0? |
| **Niedrig** | Kosmetik, Extras, "Wäre schön" | Verschieben auf v2.0 |

---

## 6. Change-Statistik

**Übersicht aller Change Requests (wird automatisch aktualisiert):**

- **Gesamt:** 0
- **Offen:** 0
- **Akzeptiert:** 0
- **Umgesetzt:** 0
- **Abgelehnt:** 0
- **Verschoben (v2.0):** 0

**Durchschnittliche Bearbeitungszeit:** -

---

## 7. Lessons Learned

**Nach Projektabschluss:**

- Welche CRs hätten wir früher erkennen können?
- Welche CRs waren überflüssig?
- Verbesserungen für nächstes Projekt?

*[Wird in Phase 8 / Projektabschluss ausgefüllt]*

---

## 8. Änderungshistorie

| Version | Datum | Autor | Änderung |
|---------|-------|-------|----------|
| 1.0 | 2024-03-28 | Claude AI | Initiale Erstellung, Template angelegt |

---

**Review-Termine:**

- **Wöchentlich:** Neue CRs sichten, priorisieren
- **Nach jedem Gate:** Alle offenen CRs bewerten

**Nächster Review:** KW 14 (nach Phase 0)

