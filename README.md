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
├── VISION.md                           # Sonorant Sound experiential goals and design parameters
├── DEVLOG.md                           # Chronological decision log
├── STANDARDS.md                        # Uniform Data Standard v1.1
├── AGENT_PLAN.md                       # Research agent specification
├── .gitignore
│
├── knowledge/                          # Verified research entries (populated by future directives)
│   ├── _research_queue.md              # Topics queued for investigation
│   ├── acoustics/_README.md
│   ├── transducers/_README.md
│   ├── psychoacoustics/_README.md
│   ├── enclosures/_README.md
│   ├── signal_processing/_README.md
│   ├── materials/_README.md
│   └── references/_README.md
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
│   ├── 001–005_directive.md / response.md
│   └── (communication between Claude instances)
│
├── schema/
│   └── company_queue.jsonl             # Master list of companies to research
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

1. **Populate knowledge base** — Begin verified research on high-priority queue topics (see `knowledge/_research_queue.md`)

2. **Batch 2 company research** — Additional boutique manufacturers or major manufacturer baselines

3. **Design synthesis** — Cross-reference company report findings with knowledge base entries
