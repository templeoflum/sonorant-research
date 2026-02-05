# sonorant-research

Research foundation for **Sonorant Sound** — a boutique communal sound system designed for psychoacoustic immersion in 100–200 capacity gatherings. This repository collects verified technical knowledge, manufacturer analysis, and design theory to inform an unconventional, experience-first approach to sound system design.

## What This Is

Sonorant Sound aims to build a transportable, high-fidelity system that prioritizes *how music feels* over how it measures. The research here spans everything needed to get there: transducer physics, enclosure theory, room acoustics, psychoacoustics, signal processing, materials science, and competitive analysis across the loudspeaker industry.

This repo is **not** a product. It's the research layer — verified, source-cited, and structured for cross-referencing.

## Current Status

| Directive | Phase | Status |
|-----------|-------|--------|
| 001 | Batch 1 company research (first half) | ✅ Complete |
| 002 | Methodology correction + Batch 1 second half | ✅ Complete |
| 003 | Score recalculation and correction pass | ✅ Complete |
| 004 | Verification sweep + repository setup | ✅ Complete |
| 005 | Vision extraction + knowledge base scaffolding | ✅ Complete |
| 006 | Process fixes + planning log introduction | ✅ Complete |

**Batch 1 Summary (8 boutique companies):**

| Rank | Company | Composite | Independent Measurements | Small-Room Viability |
|------|---------|-----------|--------------------------|----------------------|
| 1 | Danley Sound Labs | 8.58 | YES (Erin's, Merlijn) | 7/10 |
| 2 | Fulcrum Acoustic | 8.00 | Partial (audioXpress) | 8/10 |
| 3 | Funktion-One | 7.78 | NO | 6/10 |
| 4 | KV2 Audio | 7.77 | NO | 8/10 |
| 5 | HOLOPLOT | 7.73 | NO | 4/10 |
| 6 | PK Sound | 6.79 | NO | 3/10 |
| 7 | Void Acoustics | 6.55 | NO | 5/10 |
| 8 | HSD | 5.13 | NO | 2/10 |

**Knowledge base:** 7 research domains scaffolded, 47 topics queued for verified investigation.

## Project Structure

```
sonorant-research/
│
├── VISION.md                    # Experiential goals and design parameters
├── PLANNING_LOG.md              # Planning-side decisions and rationale
├── DEVLOG.md                    # Chronological decision log (8 entries)
├── STANDARDS.md                 # Uniform Data Standard (UDS) v1.1
├── AGENT_PLAN.md                # Research agent specification
├── README.md                    # This file
├── .gitignore
│
├── knowledge/                   # Verified research by domain
│   ├── _research_queue.md       # 47 topics queued (21 high / 20 med / 6 low)
│   ├── acoustics/               # Room behavior, radiation, modal analysis
│   ├── transducers/             # Driver physics, motor theory, nonlinearities
│   ├── psychoacoustics/         # Spatial hearing, immersion, tactile perception
│   ├── enclosures/              # Loading types, alignments, cardioid techniques
│   ├── signal_processing/       # Crossovers, FIR/IIR, phase alignment, TQ
│   ├── materials/               # Cone, cabinet, magnet materials
│   └── references/              # Verified bibliography index
│
├── reports/                     # Company analysis (UDS-compliant)
│   └── boutique/
│       ├── danley_sound_labs.md/.json
│       ├── fulcrum_acoustic.md/.json
│       ├── funktion_one.md/.json
│       ├── kv2_audio.md/.json
│       ├── holoplot.md/.json
│       ├── pk_sound.md/.json
│       ├── void_acoustics.md/.json
│       ├── hennessey_sound_design.md/.json
│       └── _indexes/
│           ├── companies.csv
│           └── models.csv
│
├── schema/
│   └── uds_v1.md                # UDS v1.1 — data standard for all records
│
├── handoff/                     # Directive/response pairs (inter-agent comms)
│   └── 001–005_directive.md / response.md
│
└── reference_raw/               # .gitignored — unverified conversation logs
```

## Research Domains

The knowledge base covers seven areas, each with defined scope and entry standards:

| Domain | Focus | Queue |
|--------|-------|-------|
| **Psychoacoustics** | Spatial hearing, HRTF, immersion, infrasonic perception, masking | 8 topics |
| **Enclosures** | Tapped horn, Paraflex, passive cardioid, horn profiles, port behavior | 12 topics |
| **Transducers** | Thiele-Small, Klippel nonlinearities, compression drivers, coaxials | 9 topics |
| **Signal Processing** | FIR/IIR crossovers, temporal EQ, cardioid processing, phase alignment | 6 topics |
| **Acoustics** | Small-room modes, boundary coupling, near/far-field, diffraction | 5 topics |
| **Materials** | Cone/diaphragm, cabinet construction, thermal management | 3 topics |
| **References** | Verified bibliography (Beranek, Toole, Leach, Klippel, etc.) | 4 topics |

Knowledge entries are populated only through verified research with source citations and confidence tagging. The directories are currently scaffolded with templates — no speculative content from conversation logs has been imported.

## Company Research Scope

Batch 1 covered 8 boutique manufacturers. The full company queue spans **160+ entities** across:

- **Pro touring & install** — d&b, L-Acoustics, Meyer, Adamson, Martin Audio, EAW, etc.
- **Boutique & bass culture** — Funktion-One, Void, Danley, KV2, HSD, RC Audio
- **Car audio & SPL** — Sundown, Digital Designs, DC Audio, Fi, JL Audio, etc.
- **Home & cinema** — KEF, Genelec, Krix, Perlisten, JTR, Grimani, etc.
- **Industrial & mass notification** — LRAD/Genasys, Federal Signal, Whelen, etc.
- **Parametric & directional** — Holosonics, Panphonics, Focusonics
- **Omnidirectional** — MBL, German Physiks, Duevel
- **Underwater** — Lubell Labs, Clark Synthesis
- **BMR & bending wave** — Tectonic Audio Labs, Manger
- **DIY** — DIY Sound Group, GSG Audio (MartySub)
- **Steerable columns** — Renkus-Heinz, Fohhn, K-array

Company reports follow the UDS (Uniform Data Standard) with 5-criterion R&D relevance scoring, source provenance, and architecture-agnostic evaluation.

## How to Read Reports

Each company has two files:

- `.md` — Human-readable dossier: history, philosophy, flagship products, patents, case studies, R&D scoring
- `.json` — Structured data following the UDS schema

The `_indexes/` folder has flat CSVs for sorting and filtering across companies and models.

## Standards

See `STANDARDS.md` (or `schema/uds_v1.md`) for the Uniform Data Standard v1.1, which defines:

- Company and model record schemas
- 5-criterion R&D relevance scoring (HF clarity, directivity, sub/infrasonic, psychoacoustic potential, small-room viability)
- Controlled tech vocabulary for cross-brand comparison
- Source provenance and confidence tagging
- Quality assurance checklist

## What's Next

1. **Populate knowledge base** — Begin verified research on high-priority queue topics (psychoacoustics and enclosures first, highest relevance to experiential goals)
2. **Batch 2 company research** — Additional manufacturers or major baselines (d&b, L-Acoustics, Meyer as reference points)
3. **Design synthesis** — Cross-reference company findings with knowledge base to identify candidate topologies for Sonorant Sound

Path 1 is recommended before path 3 — design synthesis requires a verified knowledge base to draw from.

## Key Documents

| File | Purpose |
|------|---------|
| `VISION.md` | What Sonorant Sound is trying to achieve — experiential goals, sonic priorities, constraints |
| `DEVLOG.md` | Chronological record of every decision, correction, and finding |
| `AGENT_PLAN.md` | Specification for the research agent that generates reports |
| `knowledge/_research_queue.md` | 47 topics queued for verified investigation |
| `PLANNING_LOG.md` | Why decisions were made — planning-side rationale and scope changes |
