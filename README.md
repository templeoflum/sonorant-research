# sonorant-research

Research archive for boutique loudspeaker company analysis. Private working repository.

## Current Status

- Batch 1 complete (8 companies)
- Correction pass complete (Directive 003)
- Verification sweep complete (Directive 004)

### Score Summary (Batch 1)

| Rank | Company | Composite | Patents (confirmed) | Independent Measurements | Small-Room Viability |
|------|---------|-----------|---------------------|--------------------------|----------------------|
| 1 | Danley Sound Labs | 8.58 | 5 (3+2 pending) | YES (Erin's, Merlijn) | 7/10 |
| 2 | Fulcrum Acoustic | 8.00 | 1 | Partial (audioXpress) | 8/10 |
| 3 | KV2 Audio | 7.77 | 0 | NO | 8/10 |
| 4 | Funktion-One | 7.78 | 1 (8+ claimed) | NO | 6/10 |
| 5 | HOLOPLOT | 7.73 | 1 | NO | 4/10 |
| 6 | PK Sound | 6.79 | 2 | NO | 3/10 |
| 7 | Void Acoustics | 6.55 | 0 | NO | 5/10 |
| 8 | HSD | 5.13 | 0 | NO | 2/10 |

**Batch 1 Average:** 7.29/10

---

## File Structure

```
sonorant-research/
├── README.md                           # This file
├── DEVLOG.md                           # Chronological decision log
├── AGENT_PLAN.md                       # Research agent specification
├── .gitignore
│
├── schema/
│   └── uds_v1.md                       # STANDARDS — Uniform Data Standard v1.1
│
├── reports/
│   └── boutique/
│       ├── danley_sound_labs.md/.json
│       ├── fulcrum_acoustic.md/.json
│       ├── funktion_one.md/.json
│       ├── hennessey_sound_design.md/.json
│       ├── holoplot.md/.json
│       ├── kv2_audio.md/.json
│       ├── pk_sound.md/.json
│       ├── void_acoustics.md/.json
│       └── _indexes/
│           ├── companies.csv
│           └── models.csv
│
├── handoff/
│   ├── 001_directive.md / 001_response.md
│   ├── 002_directive.md / 002_response.md
│   ├── 003_directive.md / 003_response.md
│   └── 004_directive.md / 004_response.md
│
├── seed/
│   └── (initial research seeds)
│
└── reference_raw/                      # .gitignored — unverified conversation logs
```

---

## How to Read Reports

Each company has two files:
- `.md` — Human-readable dossier with product specs, case studies, patents, and R&D analysis
- `.json` — Structured data following the UDS schema

The `_indexes/` folder contains flat CSVs for sorting and filtering:
- `companies.csv` — One row per company with scores and key attributes
- `models.csv` — One row per documented product with specifications

---

## Standards

See `schema/uds_v1.md` for the Uniform Data Standard (UDS) v1.1.

The UDS defines:
- Company and model record schemas
- 5-criterion R&D relevance scoring system
- Tech vocabulary for cross-brand comparisons
- Source provenance and confidence tagging
- Quality assurance checklist

---

## Devlog

See `DEVLOG.md` for chronological record of decisions, rationale, and findings throughout the research process.

---

## What's Next

Three candidate paths for Batch 2:

1. **Go wide** — Additional boutique manufacturers (Alcons, Turbosound, Radian, Amate Audio, Kling & Freitag, etc.)

2. **Go deep** — Technology deep-dives:
   - Passive cardioid design (Fulcrum patent analysis)
   - Coaxial point source architectures
   - TQ/FIR temporal correction
   - Tapped horn loading
   - Wave field synthesis fundamentals

3. **Go reference** — Major manufacturers as comparison baselines:
   - d&b audiotechnik
   - L-Acoustics
   - Meyer Sound
   - JBL Professional
