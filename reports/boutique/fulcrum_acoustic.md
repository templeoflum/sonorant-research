# Fulcrum Acoustic — Company Dossier

**Company ID:** `fulcrum_acoustic`
**Founded:** 2008
**HQ:** Whitinsville, Massachusetts, USA
**Status:** Active, Private (LLC)

---

## Company Overview

Fulcrum Acoustic was founded in 2008 by Stephen Siegel, David Gunness, and Chris Alfiero. The founders met in the early 1990s when Siegel was a consultant at Acentech and Gunness/Alfiero worked at Electro-Voice. Siegel and Gunness later worked together at Eastern Acoustic Works (EAW). In 2007, Alfiero (then in finance) reconnected with the pair and provided seed capital to form Fulcrum.

The company positions itself as "installation-focused" rather than touring-focused, emphasizing architectural compatibility and integrator-friendly design. All products are designed and manufactured in Massachusetts.

### Key People

| Name | Role | Background |
|------|------|------------|
| Stephen Siegel | President | Former consultant at Acentech; EAW engineering; University of Rochester/Eastman School of Music |
| David Gunness | VP of R&D, Chief Designer | 12 years at EAW; developed "Gunness Focusing"; multiple patents; Electro-Voice |
| Chris Alfiero | Co-founder | Electro-Voice sales/distribution; finance background |

---

## Design Philosophy

**Tags:** `coaxial`, `passive_cardioid`, `temporal_equalization`, `dsp_integrated`, `pattern_control`

Fulcrum treats loudspeakers and DSP as a unified system rather than separate components. Key principles:

1. **TQ as Foundation:** Temporal Equalization allows use of optimal loudspeaker design characteristics while eliminating natural resonances through DSP
2. **Passive Cardioid Innovation:** Mechanical directional control without requiring dual drivers or active arrays
3. **Coaxial Focus:** Comprehensive coaxial product range unique in the industry
4. **Installation-First:** "Many of our products started as custom solutions for specific projects" — Stephen Siegel

### Notable Quotes

> "We treat both loudspeakers and DSP as one system."
> — Fulcrum Acoustic [1]

> "Loudspeakers tuned with TQ provide a crisper stereo image, greater soundstage depth, more separation between the elements of a complex mix."
> — Fulcrum Acoustic [2]

---

## Core Technologies

### 1. Temporal Equalization (TQ)
- **Developer:** David Gunness (evolved from "Gunness Focusing" at EAW)
- **Principle:** FIR filter-based DSP that eliminates temporal distortion by applying reverse image of expected speaker response
- **Levels:**
  - Level 2: Standard IIR filters (high-pass, low-pass, parametric) + delay — compatible with most DSP platforms
  - Level 1: FIR + IIR filters for highest fidelity
- **Benefits:** Crisper imaging, soundstage depth, separation, feedback resistance, seamless distributed systems

### 2. Passive Cardioid Technology (US10,123,111 B2)
- **Patent:** US10,123,111 B2, granted November 6, 2018
- **Inventor:** David W. Gunness
- **Principle:** Acoustic circuit using rear-mounted ports with calibrated resistive elements to create subcardioid pattern
- **Performance:** 6+ dB attenuation across 150° rear hemisphere from 50-250 Hz; 10 dB rear rejection in operating range
- **Advantage:** Achieves cardioid behavior in half the space of active cardioid arrays, without additional amplifier channels

### 3. Coaxial Driver Design
- **Implementation:** Pattern-control coaxial drivers with Occulus Phase Plug
- **Range:** Multiple driver sizes/configurations and horn patterns — "comprehensive range unique in the industry"
- **Benefit:** True point-source behavior with consistent pattern through crossover

---

## Product Lines

### FH Series (Full-Range Coaxial Horn)

| Model | Coverage | Bandwidth | Max SPL | Power | Z | Drivers | Notes |
|-------|----------|-----------|---------|-------|---|---------|-------|
| **FH1565** | 60°×45° | 54Hz–20kHz | 138/132 dB | 800W | 8Ω | 15" (3.5" VC) + 4" Ti CD | Pattern control to 400Hz |
| **FH1566** | 60°×60° | 54Hz–20kHz | 138/132 dB | 800W | 8Ω | 15" (3.5" VC) + 4" Ti CD | 35° trapezoidal |
| **FH1596** | 90°×60° | 54Hz–20kHz | 138/132 dB | 800W | 8Ω | 15" (3.5" VC) + 4" Ti CD | Wide coverage |

*Spec provenance: Manufacturer. Single-amplified with DSP.*

### CS Series (Passive Cardioid Subwoofers)

| Model | Operating Range | Rear Rejection | Max SPL | Power | Z | Driver | Notes |
|-------|-----------------|----------------|---------|-------|---|--------|-------|
| **CS118** | 29Hz–137Hz | 10 dB | 136/130 dB (half-space) | 1200W | 8Ω | 18" (4" VC) ceramic | Sensitivity: 103 dB (half-space) |
| **CS121** | ~25Hz–137Hz | 10 dB | — | — | — | 21" | Patented passive cardioid |

*Spec provenance: Manufacturer + distributor listings. Independent validation via audioXpress patent review.*

### FL283 (Subcardioid Line Array)

| Model | Coverage | Operating Range | Max SPL | Power | Z | Drivers |
|-------|----------|-----------------|---------|-------|---|---------|
| **FL283** | 90°H, array-dependent V | 54Hz–18.6kHz | — | — | 16Ω | 2×8" (2" VC) + 3×1.4" Ti CD |

*Spec provenance: Manufacturer. First product with Passive Cardioid Technology.*

### TQ Install Series (Compact Coaxial)

- Multiple driver sizes for installation applications
- TQ processing standard
- Pattern options from narrow to wide

---

## Patents Summary

| Patent | Year | Title | Technology |
|--------|------|-------|------------|
| US10,123,111 B2 | 2018 | Passive Cardioid Speaker | Acoustic circuit for directional LF control |
| (EAW era) | 1997 | Downfill loudspeaker | Sound direction without rigging changes |
| (EAW era) | 1997 | Common acoustical wavefront | Horizontally arrayed horns |

*Note: David Gunness filed 3 patents at EAW plus the Passive Cardioid patent at Fulcrum.*

---

## Case Studies

### Avalon and Pangaea (Singapore)

- **Type:** High-energy nightclubs
- **System:** Prophile XL, L, M series coaxials + FA Portable subs
- **Requirements:** Elevated SPL, visceral LF punch for massive dance floor
- **Outcome:** Clarity and precise directional control from compact, low-profile enclosures
- **Source:** [3]

### Anthology (Rochester, NY)

- **Type:** Performing arts club
- **System:** 2× CX1295 12" coaxial + dual 8" delays + FW15 cardioid stage monitors
- **Focus:** Enhanced artist monitoring, sophisticated shows
- **Source:** [4]

### Jersey Shore Wedding Venues

- **Venues:** Crystal Point Yacht Club, The English Manor
- **System:** Compact Fulcrum installation loudspeakers
- **Goal:** "Nightclub feel" with controlled volume
- **Integrator:** Synapse Audio Visual Designs
- **Source:** [5]

---

## Technical Observations

### Strengths
- **Passive Cardioid:** Patented, proven 10 dB rear rejection without active arrays
- **TQ Processing:** Sophisticated FIR-based temporal correction
- **Coaxial Expertise:** Industry-leading range of coaxial configurations
- **Installation Focus:** Products designed for real-world architectural integration

### Data Gaps
- **No Independent Measurements:** No third-party Klippel or similar measurements found
- **Limited Club Case Studies:** Primarily sports/performing arts venues; fewer EDM/club references
- **Weight/Dimensions:** Many product pages lack complete mechanical specifications

---

## R&D Relevance to Sonorant

| Criterion | Score (0-10) | Rationale |
|-----------|--------------|-----------|
| HF clarity & transient | 8 | TQ processing specifically targets temporal distortion; coaxial point-source coherence |
| Directivity control & imaging | 9 | Pattern control to 400Hz with coaxials; passive cardioid for LF control; imaging benefits from TQ |
| Sub-weight & infrasonic | 7 | CS118 reaches 29Hz; passive cardioid achieves cardioid in compact single-box |
| Psychoacoustic potential | 8 | TQ claims: "crisper stereo image, greater soundstage depth, separation between elements" |
| Small-room viability | 8 | Installation-focused; TQ Install series designed for venues; FW15 cardioid monitor |

**Composite Score:** 8.00/10

**Key Takeaways for Sonorant:**
1. **Passive Cardioid Patent:** US10,123,111 is highly relevant for sub design — achieves directional control mechanically
2. **TQ Processing Philosophy:** Treating speaker+DSP as unified system aligns with MEH approach
3. **Coaxial Expertise:** Extensive pattern-controlled coaxial designs worth studying
4. **FH1566:** 54Hz–20kHz coaxial horn with 60°×60° coverage — potential reference for full-range point source
5. **David Gunness Background:** Track record at EAW, published patents, technical credibility

---

## Sources

1. [Fulcrum Acoustic: Company](https://www.fulcrum-acoustic.com/professional-loudspeaker-manufacturer/)
2. [Fulcrum Acoustic: TQ Implementation](https://fulcrum-acoustic.com/wp-content/uploads/2019/10/implement-tq-processing.pdf)
3. [Fulcrum Acoustic: Avalon and Pangaea Case Study](https://www.fulcrum-acoustic.com/case-studies/avalon-and-pangaea/)
4. [Fulcrum Acoustic: Anthology Case Study](https://www.fulcrum-acoustic.com/case-studies/anthology/)
5. [Installation International: Jersey Shore Wedding Venues](https://www.installation-international.com/case-studies/fulcrum-acoustic-brings-night-club-quality-to-sound-to-jersey-shore-wedding-venue)
6. [audioXpress: Patent Review - Passive Cardioid Speaker](https://audioxpress.com/article/patent-review-passive-cardioid-speaker)
7. [ProSoundWeb: Fulcrum Acoustic Patent Announcement](https://www.prosoundweb.com/fulcrum-acoustic-awarded-patent-for-passive-cardioid-loudspeaker/)
8. [Parsons Audio: FH15 Specifications](https://paudio.com/product/fulcrum-acoustic-fh15-full-range-coaxial-horn/)
9. [Parsons Audio: CS118 Specifications](https://paudio.com/product/fulcrum-acoustic-cs118-18%E2%80%B3-subcardioid-subwoofer/)
10. [MONDO-DR: In Profile Fulcrum Acoustic](https://www.mondodr.com/in-profile-fulcrum-acoustic/)
11. [Fast and Wide: CS118/CS121 Announcement](https://www.fast-and-wide.com/equipment-releases/loudspeakers-sound-reinforcement/8756-fulcrum-acoustic-cs118-cs121-cardioid-subwoofers)
12. [Justia: David W. Gunness Patents](https://patents.justia.com/inventor/david-w-gunness)

---

## Audit Notes

- **Source Count:** 12 (meets threshold)
- **Independent Measurements:** None found. audioXpress patent review provides technical validation of passive cardioid claims.
- **Patent Verified:** US10,123,111 B2 confirmed via USPTO/audioXpress review
- **Gaps:** Many product pages returned 404 errors; specs gathered from distributor sites. Weight/dimensions incomplete for most models. Limited club/EDM case studies.
- **Provenance:** All specs from manufacturer or authorized distributors; no third-party verification of SPL/sensitivity.
- **last_audited:** 2025-02-05
