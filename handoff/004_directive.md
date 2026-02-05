# Directive 004 — Repository Setup, Verification Sweep & Standards Alignment

**From:** Planning instance (claude.ai)  
**To:** Transducer Archive (CLI agent)  
**Date:** 2025-02-05

## Objective

Three tasks in order:
1. **Verify** data integrity across all 8 reports and fix any issues found
2. **Align** STANDARDS.md with actual practice (resolve spec-vs-reality drift)
3. **Scaffold** the GitHub repository with README, DEVLOG, indexes, and .gitignore

No new research. No new companies. This is infrastructure and QA.

---

## PART A: Verification Sweep (All 8 Reports)

The correction pass in Directive 003 verified scores for Danley, Funktion-One, and Void. Reports 4–8 have never been audited for math accuracy. Additionally, we need to verify cross-report consistency.

### A1. Composite Score Math Verification

Recalculate the composite score for **all 8 companies** using the weights from their own JSON files. Show your math in the response document.

Formula: `composite = Σ(score_i × weight_i)`

For each company:
- Extract scores and weights from JSON
- Calculate expected composite
- Compare to stored `composite` value
- Flag any discrepancy > 0.01
- Fix the JSON and markdown if discrepancy found

### A2. JSON Schema Consistency Check

Verify all 8 JSON files contain the same top-level fields. Produce a table showing:

| Field | danley | funktion_one | void | kv2 | fulcrum | pk_sound | holoplot | hsd |
|-------|--------|--------------|------|-----|---------|----------|---------|-----|
| spec_provenance_note | ✅/❌ | ... | ... | ... | ... | ... | ... | ... |
| audit_notes | ✅/❌ | ... | ... | ... | ... | ... | ... | ... |
| last_audited | ✅/❌ | ... | ... | ... | ... | ... | ... | ... |
| (etc.) | | | | | | | | |

Flag any missing fields and add them.

### A3. Scoring Weight Consistency

Verify all 8 JSON files use **identical** scoring criteria and weights. Report:
- Which criteria each file uses
- The weights for each
- Any file that deviates

All files must use the same 5-criterion system:
```
hf_clarity_transient:        0.23
directivity_control_imaging: 0.23
sub_weight_infrasonic:       0.23
psychoacoustic_potential:    0.20
small_room_viability:        0.11
```

If any file still has `modularity_transport` or different weights, fix it and recalculate the composite.

### A4. Spec Provenance & Units Spot Check

For each of the 8 markdown reports, verify:
- [ ] Every product spec table has a `*Spec provenance:*` note below it
- [ ] Units are metric-first with imperial in parentheses throughout
- [ ] No scoring rationale references MEH as a benchmark or assumed topology

Report any failures and fix them.

### A5. Danley Small-Room Rationale Fix

Known issue from review: `danley_sound_labs.json` field `r_and_d_relevance.rationale.small_room_viability` still reads "SM60F at 50lbs" — should be metric-first: "SM60F at 22.7 kg (50 lbs)". Fix this.

---

## PART B: Standards Alignment

### B1. Update STANDARDS.md

The current STANDARDS.md (formerly `sound_company_deep_dive_agent.md`) contains the **old 6-criterion scoring system** with `modularity_transport` and weights that don't match actual practice.

Update Section 5 (R&D relevance scoring) to reflect the current 5-criterion system:

```json
{
  "scores": {
    "hf_clarity_transient": 0.0,
    "directivity_control_imaging": 0.0,
    "sub_weight_infrasonic": 0.0,
    "psychoacoustic_potential": 0.0,
    "small_room_viability": 0.0
  },
  "weights": {
    "hf_clarity_transient": 0.23,
    "directivity_control_imaging": 0.23,
    "sub_weight_infrasonic": 0.23,
    "psychoacoustic_potential": 0.20,
    "small_room_viability": 0.11
  },
  "composite": 0.00,
  "rationale": {
    "hf_clarity_transient": "driver/waveguide clarity, transient response, HD data",
    "directivity_control_imaging": "pattern control, imaging stability, beam steering capability",
    "sub_weight_infrasonic": "LF extension, efficiency-to-weight ratio, infrasonic capability",
    "psychoacoustic_potential": "immersion, spatial perception, soundstage depth",
    "small_room_viability": "suitability for 100-200 cap venues, cardioid/dipole/low group delay"
  }
}
```

Also update `r_and_d_flags` in Section 6 to remove `transport_modular` and `synergy_candidate` (architecture-specific). Replace with architecture-neutral flags:
```
R&D flags: infra_ready | cardioid_capable | psychoacoustic_potential | temporal_correction | passive_directivity | coaxial_coherent | ob_hybrid_candidate
```

Add a version note at the top of STANDARDS.md:
```
**UDS Version:** 1.1 (updated 2025-02-05)
**Changelog:** Removed modularity_transport criterion; updated weights to 5-criterion system; removed architecture-specific R&D flags.
```

### B2. Rename File

The file is currently `sound_company_deep_dive_agent.md`. Rename to `STANDARDS.md` in the repo structure. Note this in your response — the user will handle the actual file rename during repo setup.

---

## PART C: Repository Scaffolding

The user will create the GitHub repo and handle git operations. Your job is to **generate the content files** that go into the repo. The user has `gh` CLI and SSH configured.

### C1. Target Structure

```
sonorant-research/
├── README.md
├── DEVLOG.md
├── STANDARDS.md                        # updated from sound_company_deep_dive_agent.md
├── .gitignore
│
├── reports/
│   ├── danley_sound_labs.md
│   ├── danley_sound_labs.json
│   ├── fulcrum_acoustic.md
│   ├── fulcrum_acoustic.json
│   ├── funktion_one.md
│   ├── funktion_one.json
│   ├── hennessey_sound_design.md
│   ├── hennessey_sound_design.json
│   ├── holoplot.md
│   ├── holoplot.json
│   ├── kv2_audio.md
│   ├── kv2_audio.json
│   ├── pk_sound.md
│   ├── pk_sound.json
│   ├── void_acoustics.md
│   ├── void_acoustics.json
│   └── _indexes/
│       ├── companies.csv
│       └── models.csv
│
├── handoffs/
│   ├── 001_directive.md
│   ├── 001_response.md
│   ├── 002_directive.md
│   ├── 002_response.md
│   ├── 003_directive.md
│   ├── 003_response.md
│   ├── 004_directive.md
│   └── 004_response.md
│
├── seed/
│   └── speaker_companies.md
│
└── reference_raw/                      # .gitignored
    └── conversation_logs.md
```

### C2. Generate .gitignore

```
# Raw reference material (large, not version-tracked)
reference_raw/

# OS files
.DS_Store
Thumbs.db

# Editor files
*.swp
*.swo
*~
```

### C3. Generate README.md

Write a README with the following sections. Keep it factual and operational — no vision statements or philosophy.

**Title:** `sonorant-research`

**Description:** One line — "Research archive for boutique loudspeaker company analysis. Private working repository."

**Current Status:**
- Batch 1 complete (8 companies)
- Correction pass complete (Directive 003)
- Verification sweep complete (Directive 004)
- Include the corrected score table:

| Rank | Company | Composite | Patents (confirmed) | Independent Measurements | Small-Room Viability |
|------|---------|-----------|---------------------|--------------------------|---------------------|
| 1 | Danley Sound Labs | 8.58 | 5 (3+2 pending) | YES (Erin's, Merlijn) | 7/10 |
| 2 | Fulcrum Acoustic | 8.02 | 1 | Partial (audioXpress) | 8/10 |
| 3 | KV2 Audio | 7.82 | 0 | NO | 8/10 |
| 4 | Funktion-One | 7.78 | 1 (8+ claimed) | NO | 6/10 |
| 5 | HOLOPLOT | 7.73 | 1 | NO | 4/10 |
| 6 | PK Sound | 6.64 | 2 | NO | 3/10 |
| 7 | Void Acoustics | 6.55 | 0 | NO | 5/10 |
| 8 | HSD | 5.13 | 0 | NO | 2/10 |

Use the verified scores from Part A — if any changed, update this table.

**File Structure:** Brief description of each directory and what it contains.

**How to Read Reports:** Each company has a `.md` (human-readable dossier) and `.json` (structured data). The `_indexes/` folder has flat CSVs for sorting and filtering.

**Standards:** Link to STANDARDS.md — describes the Uniform Data Standard (UDS) the agent operates under.

**Devlog:** Link to DEVLOG.md — chronological record of decisions, rationale, and findings.

**What's Next:** Three candidate paths for Batch 2 (do not choose — just list):
1. Go wide — additional boutique manufacturers
2. Go deep — technology deep-dives (passive cardioid, coaxial, TQ processing, tapped horn)
3. Go reference — major manufacturers (d&b, L-Acoustics, Meyer) as comparison baselines

### C4. Generate DEVLOG.md

Chronological, append-only log. Write entries for each phase so far. Each entry should have:
- **Date**
- **Phase/Directive reference**
- **What happened** (factual)
- **Key decisions and rationale** (why we chose what we chose)
- **Surprises or pattern shifts** (what we didn't expect)
- **Open questions** (what remained unresolved)

**Entries to write:**

**Entry 1 — Project Inception**
- Distilling raw conversation material into structured research plan
- Creation of UDS spec
- Selection of pilot batch (8 boutique companies)
- Rationale for company selection: mix of established (Danley, Funktion-One), emerging (Fulcrum, KV2), scale-contrast (HOLOPLOT, PK Sound), aesthetic (Void), niche (HSD)
- Decision to start with boutique over majors

**Entry 2 — Batch 1, First Half (Directive 001)**
- Danley, Funktion-One, Void completed
- Danley emerged as MEH/Synergy Horn anchor with independent measurements
- Funktion-One established as bass culture reference
- Void flagged as aesthetic-only — thin on verifiable tech
- Initial scoring used MEH as implicit benchmark (later corrected)

**Entry 3 — Course Correction (Directive 002)**
- Identified three issues: no spec provenance, imperial-first units, MEH-biased scoring
- Decision to score against experiential goals not assumed topology
- Dropped `modularity_transport` criterion (architecture-specific)
- Redistributed weights to 5-criterion system
- Instructed agent to stop scoring against MEH

**Entry 4 — Batch 1, Second Half (Directive 002 continued)**
- KV2, Fulcrum, PK Sound, HOLOPLOT, HSD completed
- **Key finding:** Fulcrum's passive cardioid patent (US10,123,111 B2) — most directly relevant innovation for small-room sub design
- **Key finding:** Directivity control spectrum emerged (mechanical-acoustic → mechanical-robotic → DSP-hybrid → full DSP)
- **Key finding:** Patent claims vs. reality gap — "proprietary" often means trade secret, not patented
- **Key finding:** Only Danley has independent measurements — single biggest differentiator in dataset
- HOLOPLOT's Sphere acquisition flagged as risk to commercial availability
- Small-room suitability ranking crystallized: Fulcrum, Danley, KV2 as top three

**Entry 5 — Correction Pass (Directive 003)**
- Brought Danley, Funktion-One, Void to Batch 2 standard
- All three composite scores were wrong (rounding errors) — recalculated
- MEH reference removed from Void's scoring rationale
- Audit notes restructured for consistency
- Dataset now at parity across all 8 reports

**Entry 6 — Verification & Repo Setup (Directive 004)**
- Found STANDARDS.md still had old 6-criterion scoring (drift from actual practice)
- Verified scores across all 8 reports
- Set up repository structure for version tracking
- Document what this entry covers based on actual work done

### C5. Generate companies.csv

One row per company. Columns:

```
company_id,name,founded_year,hq_country,composite_score,hf_clarity,directivity_control,sub_weight,psychoacoustic,small_room,patent_count_confirmed,independent_measurements,key_technology,last_audited
```

Pull values from the JSON files. `patent_count_confirmed` = only verified granted patents (not claimed or pending). `independent_measurements` = yes/partial/no.

### C6. Generate models.csv

One row per product documented across all 8 reports. Columns:

```
model_id,company_id,model_name,form_factor,bandwidth_low_hz,bandwidth_high_hz,sensitivity_db,max_spl_peak_db,weight_kg,directivity_nominal,small_room_relevant,spec_provenance
```

`small_room_relevant` = yes/no based on whether the product is realistic for 100–200 cap venues (consider weight, output, intended application). `spec_provenance` = manufacturer/independent/distributor.

Include all products that have enough data to populate at least 4 of the spec columns. Skip products with only a name and no specs.

---

## PART D: Vision Alignment Check

Before finalizing, review the scoring rationale across all 8 reports one more time against the core experiential goals for Sonorant:

- **Hyper-real clarity** — crystal clear vocals, high resolution for intricate soundscapes
- **Sub weight** — tactile, chest-presence bass with infrasonic extension
- **Psychoacoustic immersion** — spatial depth, envelopment, the "audio moment"
- **Small-room optimization** — 100–200 cap, reflection control, stage bleed management
- **Fast transients** — snap, articulation, dynamic punch

If any company's scoring rationale doesn't clearly connect to these goals, rewrite it. The rationale should explain *why* a score was given in terms the experiential goals above — not in terms of specs alone. "Reaches 29Hz" is a spec. "Reaches 29Hz, providing tactile sub-bass presence for small-room electronic music" connects the spec to the goal.

Do NOT change scores — only rewrite rationale text to be goal-connected where it isn't already.

---

## Scope Boundaries

- **DO:** Verify, fix, and generate all files listed above
- **DO:** Show all composite score math in the response
- **DO:** Flag any issues found during verification
- **DO NOT:** Add new companies or conduct new research
- **DO NOT:** Edit historical handoff files (001–003 responses/directives)
- **DO NOT:** Run git commands — the user handles repo creation and pushing
- **DO NOT:** Change any scores — only fix math errors and rewrite rationale text

---

## Deliverables

1. **004_response.md** containing:
   - Part A verification results (score math for all 8, schema table, weight consistency, spot check results)
   - Part B changes summary
   - Part D rationale rewrites (if any)
   - List of all files created/modified

2. **Updated files:**
   - Any JSON/MD files with issues found in Part A
   - Updated STANDARDS.md (Part B)

3. **New files:**
   - `.gitignore`
   - `README.md`
   - `DEVLOG.md`
   - `reports/_indexes/companies.csv`
   - `reports/_indexes/models.csv`

---

## Verification Checklist (Self-Check Before Submitting)

- [ ] All 8 composite scores verified with shown math
- [ ] All 8 JSON files have identical schema fields
- [ ] All 8 JSON files use identical 5-criterion weights
- [ ] STANDARDS.md updated to match actual practice
- [ ] All markdown reports have provenance notes and metric-first units
- [ ] No scoring rationale references MEH as benchmark
- [ ] All scoring rationale connects to experiential goals
- [ ] README.md contains verified score table
- [ ] DEVLOG.md has 6 entries covering full project history
- [ ] companies.csv has 8 rows with accurate data
- [ ] models.csv has all documented products with sufficient data
- [ ] .gitignore excludes reference_raw/
- [ ] No new research was conducted
- [ ] No historical handoff files were edited
