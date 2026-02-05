# Handoff 001 — Response

**From:** Transducer Archive (CLI agent)
**To:** Planning instance (claude.ai)
**Date:** 2025-02-04
**Updated:** 2025-02-04 (ongoing)

## Status: IN PROGRESS — 3/8 Companies Complete

---

## Setup Notes

### Validation Script
`validate.sh` created but requires `jq` to be installed:
```bash
choco install jq  # Windows
apt install jq    # Linux
```

---

## Pilot Batch Progress

| # | Company | Status | R&D Score | Key Technology |
|---|---------|--------|-----------|----------------|
| 1 | Danley Sound Labs | **COMPLETE** | 8.54 | Synergy Horn (MEH), Tapped Horn |
| 2 | Funktion-One | **COMPLETE** | 7.71 | Turbo mid-loading, acoustic-flat philosophy |
| 3 | Void Acoustics | **COMPLETE** | 6.43 | Fibreglass aesthetic, horn-loaded subs |
| 4 | KV2 Audio | Queued | — | — |
| 5 | Fulcrum Acoustic | Queued | — | — |
| 6 | PK Sound | Queued | — | — |
| 7 | HOLOPLOT | Queued | — | — |
| 8 | Hennessey Sound Systems | Queued | — | — |

---

## Company Summaries

### 1. Danley Sound Labs (8.54/10) — **HIGHEST RELEVANCE**

**Why It Matters:** Danley is the origin of MEH/Synergy Horn technology — the exact architecture Sonorant is exploring.

**Key Patents:**
- US6411718B1 (2002) — Synergy Horn: multiple drivers sum at single aperture
- US8457341B2 (2013) — Tapped Horn: dual-path loading for sub efficiency
- US8284976B2 (2012) — Horn coupling improvements

**Products for 100-200 Cap:**
- SM60F: 50lbs, 60x60, 66Hz-24kHz
- TH118: 160lbs tapped horn sub, 28Hz extension

**Validated Case Study:** The Love Inn (Bristol) — ~200 cap club

---

### 2. Funktion-One (7.71/10) — **REFERENCE FOR BASS**

**Design Philosophy:** "Acoustically flat" — no corrective EQ, preserves headroom. Proprietary driver design.

**Key Patent:**
- US6650760B1 (2003) — Turbo mid-loading: 107dB @ 1W/1m across 75-750Hz

**Bass Reference:**
- F121: single 21" horn-loaded, 40Hz-250Hz, 101dB sens
- F221: dual 21" horn-loaded, 104dB sens
- F132: 32" infrasonic, 20Hz-50Hz

**Contrast to MEH:** Traditional multi-box topology; no synergy/unity summation approach

---

### 3. Void Acoustics (6.43/10) — **AESTHETIC BENCHMARK**

**Design Philosophy:** "Obsessive technical innovation and extraordinary design aesthetics" — fibreglass sculptural enclosures for visual impact.

**Key Technologies:**
- Fibreglass Kevlar composite construction
- Heat Transference Technology (HTT)
- Pressure Gradient Porting

**Products:**
- Air Motion: 35.4kg, 60x50, fibreglass horn-loaded
- Stasys XV2: dual 18" horn-loaded sub, 30Hz-180Hz, 104dB
- Incubus Sub: triple 21" hybrid horn-loaded, 29Hz-95Hz, 6000W

**Relevance:** Demonstrates market demand for visually distinctive systems; not MEH architecture

---

## Cross-Company Observations

### MEH/Synergy Architecture
Only **Danley** has patented multi-entry horn / unity summation technology. Funktion-One and Void use traditional multi-box / separate horn topologies.

### Sub Architecture Comparison

| Company | Model | Type | Extension | Sensitivity | Weight |
|---------|-------|------|-----------|-------------|--------|
| Danley | TH118 | Tapped Horn | 28Hz (-10dB) | 108dB | 73kg |
| Danley | BC218 | Horn-loaded | 22Hz (-10dB) | 110dB | 232kg |
| Funktion-One | F121 | Horn-loaded | 20Hz (op) | 101dB | 72kg |
| Funktion-One | F221 | Horn-loaded | 20Hz (op) | 104dB | 130kg |
| Void | Stasys XV2 | Horn-loaded | 30Hz | 104dB | 130kg |
| Void | Incubus Sub | Hybrid bandpass | 29Hz | 105dB | 214kg |

### Small-Venue Suitability

| Company | Best Fit for 100-200 Cap | Notes |
|---------|-------------------------|-------|
| Danley | SM60F + TH118 | Validated at Love Inn |
| Funktion-One | Res 2 / Evo 6E + F218 | Careful deployment needed |
| Void | Cyclone series | Flagship products too large |

---

## Files Created

```
reports/boutique/
├── danley_sound_labs.md
├── danley_sound_labs.json
├── funktion_one.md
├── funktion_one.json
├── void_acoustics.md
└── void_acoustics.json

reports/_indexes/
├── companies.csv (3 entries)
└── models.csv (14 entries)
```

---

## Questions

None at this time. Continuing with KV2 Audio.

---

*Research continuing...*
