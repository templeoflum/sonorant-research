# Handoff 002 — Response

**From:** Transducer Archive (CLI agent)
**To:** Planning instance (claude.ai)
**Date:** 2025-02-05

## Status: BATCH 1 COMPLETE — 8/8 Companies Researched

---

## Pilot Batch Final Status

| # | Company | Status | R&D Score | Key Technology | Patents |
|---|---------|--------|-----------|----------------|---------|
| 1 | Danley Sound Labs | **COMPLETE** | 8.54 | Synergy Horn (MEH), Tapped Horn | 3 granted + 2 pending |
| 2 | Funktion-One | **COMPLETE** | 7.71 | Turbo mid-loading, no-EQ philosophy | 1 confirmed (8+ claimed) |
| 3 | Void Acoustics | **COMPLETE** | 6.43 | Fibreglass composite, aesthetic focus | 0 found |
| 4 | KV2 Audio | **COMPLETE** | 7.82 | Trans-Coil, NVPD, point-source coherence | 0 found (claims proprietary) |
| 5 | Fulcrum Acoustic | **COMPLETE** | 8.02 | TQ Processing, Passive Cardioid | 1 granted (US10,123,111 B2) |
| 6 | PK Sound | **COMPLETE** | 6.64 | Robotic beam steering, CMI Waveguide | 2 granted |
| 7 | HOLOPLOT | **COMPLETE** | 7.73 | Wave Field Synthesis, 3D Beamforming | 1 granted (EP3061271B1) |
| 8 | Hennessey Sound Design | **COMPLETE** | 5.13 | Horn-loaded subs, bass culture focus | 0 found |

**Batch 1 Average R&D Score:** 7.25/10

---

## Corrections Applied (per Directive 002)

1. **Spec Provenance:** Added `spec_provenance_note` field to all JSON files starting with KV2
2. **Metric Primary:** All new reports use kg/mm with imperial in parentheses
3. **Architecture-Agnostic Scoring:** Scored against experiential goals, not assumed topology
4. **Data Gap Documentation:** Explicit audit notes about missing independent measurements

---

## Company Summaries (New Additions)

### 4. KV2 Audio (7.82/10) — **TRANSIENT FOCUS**

**Why It Matters:** KV2's "no line array" philosophy and Trans-Coil dual voice coil technology offers an alternative point-source approach with emphasis on transient response.

**Key Technologies:**
- Trans-Coil: Dual voice coil (one for cone control, one for signal) — claimed 30% more power, 60% less distortion
- NVPD: Titanium compression driver for HF clarity
- Point Source Architecture: Explicitly rejects line array for coherence reasons

**Small-Venue Fit:**
- ESD10: 16.5kg point source, 65Hz-20kHz, 131dB peak
- ES2.5: 74.7kg horn-loaded sub, 34Hz (-10dB)

**Data Gaps:** No independent measurements; Trans-Coil patent not located despite proprietary claims

---

### 5. Fulcrum Acoustic (8.02/10) — **HIGHEST RELEVANCE (SMALL-ROOM)**

**Why It Matters:** Fulcrum's TQ (Temporal Equalization) processing and Passive Cardioid patent directly address small-room challenges: temporal distortion correction and LF directivity control without active arrays.

**Key Patent:**
- US10,123,111 B2 (2018) — Passive Cardioid Speaker: Acoustic circuit for directional LF control without active rear-firing drivers

**Key Technologies:**
- TQ Processing: FIR filter-based temporal distortion correction; claims "crisper stereo image, greater soundstage depth"
- Passive Cardioid: 10dB rear rejection in single-box subwoofer
- Comprehensive Coaxial Range: Pattern control to 400Hz

**Products for 100-200 Cap:**
- FH1566: 60x60 coaxial horn, pattern control to 400Hz
- CS118: 18" passive cardioid sub, 29Hz extension, 10dB rear rejection
- FW15: Cardioid stage monitor (reduces feedback issues)

---

### 6. PK Sound (6.64/10) — **ROBOTIC DIRECTIVITY**

**Why It Matters:** PK Sound's approach — mechanical beam steering via robotic actuators rather than DSP — represents a distinct philosophy for directivity control.

**Key Patents:**
- US20140353074A1 — Robotic mounting for line array (0.1° vertical precision)
- US9894433B2 — CMI Waveguide (60-120° horizontal variable directivity)

**Key Product:**
- T10: 47.6kg, 40Hz-20kHz, 146dB, robotic 0.1° vertical / 5° horizontal adjustment

**Relevance:** Technology optimized for festival-scale (Shambhala, EDC); not small-venue focused. Mechanical vs. DSP beam steering debate relevant to architecture decisions.

---

### 7. HOLOPLOT (7.73/10) — **WAVE FIELD SYNTHESIS BENCHMARK**

**Why It Matters:** HOLOPLOT represents the extreme end of DSP-centric sound field control — per-driver processing, Wave Field Synthesis for true virtual source positioning.

**Key Patent:**
- EP3061271B1 (2018) — Decentralized WFS system with computational scalability

**Key Technologies:**
- Wave Field Synthesis: Physical wavefront reconstruction (Huygens' principle), not psychoacoustic phantom imaging
- 3D Audio-Beamforming: 0.1° resolution, 12 independent beams per module
- Per-Driver Processing: 96 individually amplified channels (MD96)

**MSG Sphere Achievement:**
- 167,000 individually amplified drivers
- 110m throw without delay lines
- "World's largest concert-grade audio system"

**Small-Room Fit:** Limited. X2 MD30 (15.6kg, 80Hz floor) most accessible; X1 modules 100-160kg.

---

### 8. Hennessey Sound Design (5.13/10) — **BASS CULTURE NICHE**

**Why It Matters:** HSD documents the extreme LF requirements of bass music festivals and validates durability standards for outdoor applications.

**Key Products:**
- Haymaker: 70.3kg point source, 50Hz-20kHz, modular waveguides
- Sherman: 200kg 24" horn-loaded sub, 25Hz extension
- Battlehawk: 154kg 21" horn-loaded sub

**Relevance:** All products festival-scale only. No patents, no independent measurements. Validates Celestion TSQ, B&C, faitalPRO as quality driver sources.

---

## Cross-Company Comparisons

### Sub Architecture Comparison (All 8 Companies)

| Company | Model | Type | Extension | Sensitivity | Weight | Notes |
|---------|-------|------|-----------|-------------|--------|-------|
| Danley | TH118 | Tapped Horn | 28Hz (-10dB) | 108dB | 73kg | Best efficiency/weight for infrasonic |
| Danley | BC218 | Horn-loaded | 22Hz (-10dB) | 110dB | 232kg | True infrasonic capability |
| Funktion-One | F121 | Horn-loaded | 20Hz (op) | 101dB | 72kg | Classic bass culture reference |
| Funktion-One | F221 | Horn-loaded | 20Hz (op) | 104dB | 130kg | Dual 21" |
| Void | Stasys XV2 | Horn-loaded | 30Hz | 104dB | 130kg | Aesthetic enclosure |
| Void | Incubus Sub | Hybrid bandpass | 29Hz | 105dB | 214kg | Triple 21" flagship |
| KV2 | ES2.5 | Horn-loaded | 34Hz (-10dB) | — | 74.7kg | Point-source philosophy |
| Fulcrum | CS118 | Passive Cardioid | 29Hz | 103dB | — | 10dB rear rejection, single-box |
| PK Sound | G218 | Reflex | — | — | — | Cardioid-arrayable |
| HOLOPLOT | MD80-S | Matrix Array | 26Hz | — | 160kg | Integrated in full-range module |
| HSD | Sherman | Horn-loaded | 25Hz (-10dB) | — | 200kg | 24" driver, festival-scale |
| HSD | Battlehawk | Horn-loaded | 25Hz (-10dB) | — | 154kg | 21" driver |

**Key Finding:** Fulcrum CS118 offers unique passive cardioid directivity for small rooms without massive weight penalty. Danley TH118 offers best efficiency for tapped horn design.

---

### Directivity Control Technologies

| Company | Technology | Method | Resolution | Small-Room Fit |
|---------|------------|--------|------------|----------------|
| Danley | Synergy Horn | Acoustic (multi-entry) | Fixed | **High** |
| Funktion-One | Turbo Mid | Acoustic (horn) | Fixed | Medium |
| Void | Standard Horn | Acoustic | Fixed | Medium |
| KV2 | Point Source | Acoustic | Fixed | **High** |
| Fulcrum | Coaxial + TQ | Acoustic + DSP | Fixed + FIR | **High** |
| PK Sound | CMI Waveguide | Robotic (mechanical) | 5° H / 0.1° V | Low (scale) |
| HOLOPLOT | 3D Beamforming + WFS | DSP (per-driver) | 0.1° | Low (scale/cost) |
| HSD | Modular Waveguide | Acoustic (swappable) | Fixed (40/60/90°) | Low (scale) |

---

### Patent Portfolio Comparison

| Company | Confirmed Patents | Patent Focus | Independent Verification |
|---------|-------------------|--------------|------------------------|
| Danley | 5 (3 granted, 2 pending) | MEH, Tapped Horn, Lens | Erin's Audio, Merlijn van Veen |
| Funktion-One | 1 (8+ claimed) | Turbo mid-loading | None found |
| Void | 0 | — | None found |
| KV2 | 0 (claims proprietary) | — | None found |
| Fulcrum | 1 | Passive Cardioid | audioXpress patent review |
| PK Sound | 2 | Robotic steering, CMI Waveguide | None found |
| HOLOPLOT | 1 | Wave Field Synthesis | None found |
| HSD | 0 | — | None found |

---

### Small-Room Suitability Ranking (100-200 Cap)

| Rank | Company | Score | Best Products | Key Advantage |
|------|---------|-------|---------------|---------------|
| 1 | **Fulcrum Acoustic** | 8.02 | FH1566 + CS118 | TQ processing, passive cardioid, installation focus |
| 2 | **Danley Sound Labs** | 8.54 | SM60F + TH118 | MEH coherence, validated case study (Love Inn) |
| 3 | **KV2 Audio** | 7.82 | ESD10 + ES2.5 | Transient response, 16.5kg top |
| 4 | Funktion-One | 7.71 | Res 2 + F121 | Bass reference, but subs still large |
| 5 | HOLOPLOT | 7.73 | X2 MD30 | Technology impressive but 80Hz floor, cost |
| 6 | Void Acoustics | 6.43 | Cyclone series | Aesthetic appeal only advantage |
| 7 | PK Sound | 6.64 | — | Festival-scale only |
| 8 | HSD | 5.13 | — | Festival-scale only |

---

## Emerging Patterns & Surprises

### 1. Patent Gap vs. Marketing Claims

**Pattern:** Several companies claim proprietary technology but lack patent documentation.
- Funktion-One claims 8+ patents; only 1 confirmed
- KV2 claims proprietary Trans-Coil; no patent found
- Void claims HTT thermal technology; no patent found

**Implication:** Manufacturer claims require verification. "Proprietary" often means trade secret (no public documentation) rather than patented innovation.

### 2. Independent Measurements Rarity

**Pattern:** Only Danley has multiple independent third-party measurements (Erin's Audio Corner, Merlijn van Veen). All other companies rely entirely on manufacturer specifications.

**Implication:** Spec provenance remains a critical gap. Consider commissioning independent measurements for final shortlist products.

### 3. Directivity Control Spectrum

**Surprise:** Directivity control approaches span a wide spectrum:
- **Mechanical-acoustic:** Danley (multi-entry horn), Funktion-One (turbo), KV2 (point source)
- **Mechanical-robotic:** PK Sound (CMI waveguide actuators)
- **DSP-hybrid:** Fulcrum (TQ + coaxial)
- **Full DSP:** HOLOPLOT (per-driver WFS)

The mechanical vs. DSP tradeoff is a key architecture decision. PK Sound claims mechanical avoids DSP quality compromise; HOLOPLOT demonstrates extreme DSP capability.

### 4. Passive Cardioid Innovation

**Surprise:** Fulcrum's Passive Cardioid patent (US10,123,111 B2) achieves 10dB rear rejection without active arrays or rear-firing drivers. This is directly relevant to small-room stage bleed and reflections — worth deeper study.

### 5. Scale Mismatch

**Pattern:** 5 of 8 companies primarily target festival/touring scale:
- PK Sound: T10 at 47.6kg, festival focus
- HOLOPLOT: MSG Sphere flagship, modules 100-160kg
- HSD: Sherman at 200kg
- Void: Incubus at 214kg
- Funktion-One: F221 at 130kg

**Implication:** Small-venue options are limited. Danley, Fulcrum, and KV2 emerge as most relevant for 100-200 cap.

### 6. Sphere Entertainment Acquisition Impact

**Surprise:** HOLOPLOT acquired by Sphere Entertainment (May 2024). Technology may become proprietary to Sphere venues rather than commercially available.

---

## Files Created (Batch 1 Complete)

```
reports/boutique/
├── danley_sound_labs.md
├── danley_sound_labs.json
├── funktion_one.md
├── funktion_one.json
├── void_acoustics.md
├── void_acoustics.json
├── kv2_audio.md
├── kv2_audio.json
├── fulcrum_acoustic.md
├── fulcrum_acoustic.json
├── pk_sound.md
├── pk_sound.json
├── holoplot.md
├── holoplot.json
├── hennessey_sound_design.md
└── hennessey_sound_design.json

reports/_indexes/
├── companies.csv (8 entries)
└── models.csv (25 entries)
```

---

## Questions for Planning Instance

### 1. Independent Measurement Commissioning
Should we add a research task to identify labs/reviewers who could provide independent measurements for shortlisted products? Erin's Audio Corner methodology appears rigorous.

### 2. Passive Cardioid Deep Dive
Fulcrum's passive cardioid patent (US10,123,111 B2) seems highly relevant for small-room LF control. Should we add a Track B task to study this patent in detail?

### 3. Batch 2 Scope
The directive mentions Batch 2. Should this include:
- Additional boutique manufacturers?
- Major manufacturers (d&b, L-Acoustics, Meyer) for reference?
- Specific technology deep-dives (coaxial, cardioid, horn loading)?

### 4. Correction Pass
Should I retroactively add `spec_provenance_note` to the first 3 JSON files (Danley, Funktion-One, Void) for consistency?

### 5. Score Reconciliation
Directive noted Danley score inconsistency (8.54 vs 8.4). Current JSON calculates 8.5. Should I audit all composite score calculations for consistency?

---

## Batch 1 Research Complete

Awaiting Directive 003 for next steps.
