# Directive 003 — Correction Pass: Danley, Funktion-One, Void Acoustics

**From:** Planning instance (claude.ai)  
**To:** Transducer Archive (CLI agent)  
**Date:** 2025-02-05

## Objective

Bring the first three company reports (Danley Sound Labs, Funktion-One, Void Acoustics) to parity with the Batch 2 standard established in reports 4–8. **No new research.** This is an editing and normalization pass only. Do not add companies, do not start Batch 2.

---

## Task List

### 1. Spec Provenance Tagging

**Problem:** Reports 4–8 include `spec_provenance_note` inline in markdown (e.g., `*Spec provenance: Manufacturer. No independent verification.*`) and in JSON product spec sections. Reports 1–3 lack these.

**Action (Markdown):**
- Add a `*Spec provenance: [source]. [verification status].*` line below every product spec table in:
  - `danley_sound_labs.md`
  - `funktion_one.md`
  - `void_acoustics.md`
- Use the same format as KV2/Fulcrum/PK Sound/HOLOPLOT/HSD reports
- For Danley: note where independent measurements exist (Erin's Audio Corner, Merlijn van Veen) — this is a *strength* and should be flagged as such

**Action (JSON):**
- Add `"spec_provenance_note"` string field to each product entry in the JSON files
- Follow the format established in `kv2_audio.json` and later files

### 2. Metric-First Units

**Problem:** Reports 4–8 lead with metric (kg, mm) and put imperial in parentheses. Reports 1–3 may have imperial-first in places.

**Action:**
- Audit all three markdown reports for unit ordering
- Normalize to: `XX kg (YY lbs)`, `XXX mm (YY")`
- Check product tables, case study sections, and body text
- JSON files should use metric values in primary fields (weight_kg, dimensions_mm)

### 3. Architecture-Agnostic Scoring Rationale

**Problem:** Some scoring rationale text in reports 1–3 references MEH as an assumed architecture or scores relative to it.

**Specific fixes required:**

**Void Acoustics JSON** — `r_and_d_relevance.rationale.directivity_control_imaging` currently reads:
> "Point source designs with controlled patterns; not MEH architecture"

Rewrite to score against the experiential goal (directivity control and imaging quality) without reference to MEH. Example: "Standard horn-loaded point source; controlled patterns but no advanced beam steering or coaxial coherence."

**Danley JSON** — Check all rationale fields. Danley *is* MEH, so references to Synergy Horn are fine as factual description, but the scoring should be against the experiential criteria, not self-referentially about the architecture.

**Funktion-One JSON** — Check rationale fields for comparative references to MEH. Score against experiential goals directly.

### 4. Composite Score Audit

**Problem:** Danley composite appears as 8.54, 8.4, and 8.5 in different places across the project files.

**Action:**
- Recalculate all three composites using the stated weights and scores
- Formula: `composite = Σ(score_i × weight_i)`
- Current weights (from all JSON files):
  ```
  hf_clarity_transient:        0.23
  directivity_control_imaging: 0.23
  sub_weight_infrasonic:       0.23
  psychoacoustic_potential:    0.20
  small_room_viability:        0.11
  ```
- Show your math for each company
- Update JSON `composite` field to match calculated value (round to 2 decimal places)
- Update markdown composite score to match
- If any score appeared differently in `001_response.md` or `002_response.md`, note the discrepancy but do NOT edit response files (those are historical records)

### 5. Data Gap Documentation

**Problem:** Reports 4–8 have explicit, standardized audit notes about missing independent measurements, unverified patents, and incomplete specs. Reports 1–3 have audit notes but they're less structured.

**Action:**
- Rewrite `audit_notes` in all three JSON files to follow the format established in Batch 2:
  ```
  "audit_notes": "Source count: X (meets/below threshold). 
  Independent Measurements: [status]. 
  Patents Verified: [status]. 
  Gaps: [specific gaps]. 
  Provenance: [summary]."
  ```
- For Danley specifically: the audit notes should prominently flag that it is the **only company with multiple independent measurement sources** — this is the single most important differentiator in the dataset

### 6. Update `last_audited` Date

**Action:** Set `last_audited` to `2025-02-05` in all three JSON files after corrections are complete.

---

## Scope Boundaries

- **DO:** Edit existing markdown and JSON files for the three companies listed
- **DO:** Show composite score math in your response
- **DO NOT:** Add new companies or products
- **DO NOT:** Conduct new web research
- **DO NOT:** Edit `001_response.md` or `002_response.md` (historical records)
- **DO NOT:** Modify CSV index files yet (we'll do a full index rebuild after this pass)
- **DO NOT:** Start Batch 2

---

## Deliverables

1. Updated `danley_sound_labs.md` + `danley_sound_labs.json`
2. Updated `funktion_one.md` + `funktion_one.json`
3. Updated `void_acoustics.md` + `void_acoustics.json`
4. Response document (`003_response.md`) containing:
   - Composite score math for all three companies
   - Summary of changes made per file
   - Any discrepancies or ambiguities encountered
   - Confirmation of parity with Batch 2 standard

---

## Verification Checklist (Self-Check Before Submitting)

- [ ] Every product spec table in markdown has a provenance note below it
- [ ] Every JSON product section has `spec_provenance_note` field
- [ ] All units are metric-first with imperial in parentheses
- [ ] No scoring rationale references MEH as a benchmark or assumed topology
- [ ] Composite scores match calculated values (show math)
- [ ] Audit notes follow Batch 2 structured format
- [ ] `last_audited` is `2025-02-05` on all three JSON files
- [ ] No new research was conducted — edits only
