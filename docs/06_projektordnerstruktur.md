# Projektordnerstruktur: Bienenapp (BSK-App)

**Version:** 1.0  
**Datum:** 2024-03-28  

---

## Ordnerstruktur
bienenapp/
├── README.md
├── .gitignore
├── LICENSE
│
├── docs/
│   ├── 00_index.md
│   ├── 01_projektsteckbrief.md
│   ├── 02_projektplan.md
│   ├── 03_stakeholder_analyse.md
│   ├── 04_risikoanalyse.md
│   ├── 05_change_requests.md
│   ├── 06_projektordnerstruktur.md
│   │
│   ├── 01_requirements/
│   │   ├── REQ_overview.md
│   │   ├── REQ_behoerden.md
│   │   ├── REQ_funktional.md
│   │   └── REQ_nichtfunktional.md
│   │
│   ├── 02_konzept/
│   │   ├── software_architektur.md
│   │   ├── datenmodell.md
│   │   ├── technologie_entscheidung.md
│   │   └── ui_mockups/
│   │       ├── screen_01_hauptmenu.png
│   │       ├── screen_02_stockkarte.png
│   │       └── mockup_beschreibung.md
│   │
│   ├── 03_detaildesign/
│   │   ├── api_spezifikation.md
│   │   ├── datenbank_schema.sql
│   │   ├── sync_konzept.md
│   │   └── druckmodul_spezifikation.md
│   │
│   ├── 04_testing/
│   │   ├── testplan.md
│   │   ├── testcases.md
│   │   └── testreport_template.md
│   │
│   ├── 05_benutzerhandbuch/
│   │   ├── anleitung_app.md
│   │   ├── anleitung_sync.md
│   │   └── faq.md
│   │
│   └── 06_projektabschluss/
│       ├── lessons_learned.md
│       ├── wartungsplan.md
│       └── changelog.md
│
├── src/
│   ├── app/
│   │   ├── components/
│   │   ├── screens/
│   │   ├── services/
│   │   ├── models/
│   │   └── utils/
│   │
│   ├── database/
│   │   ├── schema/
│   │   │   ├── create_tables.sql
│   │   │   └── seed_data.sql
│   │   ├── migrations/
│   │   └── backup_scripts/
│   │
│   └── sync/
│       └── sync_manager.py
│
├── tests/
│   ├── unit/
│   ├── integration/
│   ├── e2e/
│   └── test_data/
│
├── assets/
│   ├── icons/
│   ├── images/
│   ├── fonts/
│   └── templates/
│
├── tools/
│   ├── db_viewer.py
│   ├── pdf_generator.py
│   └── data_import.py
│
└── releases/
    ├── v1.0.0/
    │   ├── bienenapp_v1.0.0.apk
    │   └── release_notes.md
    └── beta/
unknown
Copy
---