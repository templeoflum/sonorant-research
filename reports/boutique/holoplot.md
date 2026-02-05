# HOLOPLOT — Company Dossier

**Company ID:** `holoplot`
**Founded:** 2011
**HQ:** Berlin, Germany
**Status:** Active, Subsidiary of Sphere Entertainment Co. (acquired May 2024)

---

## Company Overview

HOLOPLOT began in 2011 as an audio research firm founded by German Tonmeister Helmut Oellers and DSP engineer Adrián Lara Moreno near Berlin. The company's core mission emerged from asking: "What if sound could truly be controlled the way we can control light?"

Helmut Oellers, the founding father of HOLOPLOT technology, took Wave Field Synthesis (WFS), merged it with 3D Audio-Beamforming, and created the Matrix Array architecture. Roman Sick joined as CEO in 2016, accelerating commercialization.

Sphere Entertainment made its first investment in 2018 when the two companies partnered to develop Sphere Immersive Sound. In May 2024, Sphere acquired all remaining shares; HOLOPLOT continues as a wholly owned subsidiary based in Berlin.

### Key People

| Name | Role | Notes |
|------|------|-------|
| Helmut Oellers | Founder, Tonmeister | Original patent holder (2004) |
| Adrián Lara Moreno | Co-Founder, DSP Engineer | Technical co-founder |
| Roman Sick | CEO | Joined 2016 |
| Philippe Robineau | Acoustic Lead | 50+ year pro audio background |
| Evert Start | DSP Lead | Wave Field Synthesis expertise |

---

## Design Philosophy

**Tags:** `wave_field_synthesis`, `3d_beamforming`, `matrix_array`, `dsp_centric`, `immersive_audio`, `sound_field_control`

HOLOPLOT treats loudspeakers as software-defined platforms. Core principles:

1. **Physical Wavefront Reconstruction:** WFS reconstructs actual wavefronts (Huygens' principle) rather than relying on psychoacoustic phantom sources
2. **3D Audio-Beamforming:** Sound beams steered independently in horizontal and vertical axes with 0.1° precision
3. **Per-Driver Processing:** Each driver individually amplified and signal-processed via FPGA
4. **Sound Field Control:** Up to 12 independent beams per module, each with separate content, EQ, level, shape, and position

### Notable Quotes

> "What if sound could truly be controlled the way we can control light?"
> — HOLOPLOT [1]

> "To make every seat the best seat."
> — HOLOPLOT core philosophy [1]

---

## Core Technologies

### 1. Wave Field Synthesis (WFS)

- **Principle:** Physically reconstructs sound fields using Huygens' principle
- **Capability:** Virtual sound sources can be positioned anywhere in 3D space
- **Advantage:** Sound objects not bound to speaker positions; move in real-time with natural Doppler effects

### 2. 3D Audio-Beamforming

- **Resolution:** 0.1° steps in both horizontal and vertical planes
- **Beams:** Up to 12 independent beams per module
- **Processing:** FPGA computes proprietary DSP algorithms in real-time
- **Filters:** 7,600 parametric EQ bands; 1,100+ FIR filters (430,000+ taps)

### 3. Inverse Wavefront Shaping

- Optimizes coverage to target zones while avoiding reflections
- Compensates for acoustic obstacles (e.g., LED screens, architectural features)

### 4. Patent Portfolio

| Patent | Year | Title | Innovation |
|--------|------|-------|------------|
| EP3061271B1 | 2018 | Wave Field Synthesis System | Decentralized modular WFS; computational scalability independent of module count |

**Inventors:** Frank Stefan Schmidt, Helmut Oellers

---

## Product Lines

### X1 Matrix Array (Large-Scale)

| Model | Type | Drivers | Bandwidth | Max SPL | Beams | Dimensions | Weight |
|-------|------|---------|-----------|---------|-------|------------|--------|
| **MD96** | Two-way | 18× 5" LF + 78× 1.3" HF | 85Hz–20kHz (-10dB) | LF: 142dB / HF: 152dB | 12 | 800 × 600 × 457 mm | 100 kg |
| **MD80-S** | Three-way | 1× 18" Sub + 16× 5" LF + 64× 1.3" HF | 26Hz–20kHz (-10dB) | Sub: 137dB / LF: 142dB / HF: 152dB | 12 | 800 × 600 × 981 mm | 160 kg |

*Spec provenance: Manufacturer. SPL values for optimized parallel beam.*

**Processing:**
- 96/82 individually amplified channels per module
- Sub amplifier: 8,500W peak (MD80-S)
- Connectivity: Dante, AES67

### X2 Matrix Array (Compact Install)

| Model | Type | Drivers | Bandwidth | Max SPL | Dimensions | Weight |
|-------|------|---------|-----------|---------|------------|--------|
| **MD30** | Full-range | 30× 2.5" | 80Hz–20kHz (-10dB ext) | 130dB (std) / 125dB (ext) | 601 × 311 × 140 mm | 15.6 kg |

*Spec provenance: Manufacturer. Two modes: Standard (140Hz floor) and Extended (80Hz floor).*

**Features:**
- PoE++ powered (802.3bt Type 4)
- Weather resistant
- AES67, RAVENNA, optional Dante
- Concealed installation behind acoustically transparent screens

---

## Case Studies

### MSG Sphere Las Vegas (2023)

- **Type:** Immersive entertainment venue
- **Capacity:** 18,600 seats
- **System:**
  - ~1,600 X1 modules (permanently installed) + 300 mobile
  - **167,000 individually amplified drivers**
  - Proscenium: 464 modules (33.6m × 6.6m)
  - Total weight: ~181,000 kg (400,000 lbs)
- **Throw:** 110m to back row without delay lines
- **Integration:** Hidden behind 16K LED media plane; algorithmic transmission loss compensation
- **Outcome:** "World's most advanced concert-grade audio system" — clear, crisp sound; earplugs unnecessary
- **Source:** [5]

### Illuminarium Experiences (Atlanta)

- **Type:** Immersive experience venue
- **System:** 360° configuration with 52× MD96 + 7× MD80-S
- **Integration:** Hidden behind micro-perforated projection screens
- **Outcome:** Virtual sound source positioning; no visible speaker localization
- **Source:** [6]

### The Portal at AREA15 (Las Vegas)

- **Type:** Entertainment venue
- **System:** 4× MD96 + 4× MD80-S (two arrays at 7.6m height)
- **Outcome:** Wall reflection mitigation; consistent audio coverage
- **Source:** [8]

### Other Deployments

- **Lightroom** (London, Seoul) — 360° immersive exhibition
- **Tomorrowland** (Belgium) — Festival Atmosphere stage
- **Masjid Misr** (Cairo) — 10,000 sqm mosque, speech intelligibility
- **St. Hedwig's Cathedral** (Berlin) — Dome acoustics challenge

---

## Technical Observations

### Strengths

- **Best-in-Class Directivity:** 0.1° beam steering resolution with independent H/V control
- **True Spatial Audio:** WFS enables virtual source positioning, not just phantom imaging
- **Scalable Architecture:** Modular design; same technology from X2 (15.6kg) to MSG Sphere (167,000 drivers)
- **DSP-Defined:** Software updates continuously improve performance
- **No Delay Lines:** 110m throw achieved at Sphere without auxiliary speakers

### Unique Value Proposition

Unlike mechanical beam steering (PK Sound) or traditional DSP beam steering (Renkus-Heinz), HOLOPLOT combines WFS for spatial positioning with beamforming for coverage control. Each driver's signal is computed individually, enabling unprecedented sound field manipulation.

### Data Gaps

- **No Independent Measurements:** All specs are manufacturer claims
- **LF Floor:** X2 limited to 80Hz (extended mode); no true sub-bass in compact format
- **Small-Venue Weight:** X1 modules 100-160kg each; X2 more accessible but limited LF
- **Cost/Accessibility:** Premium pricing limits small-venue adoption
- **Corporate Dependency:** Sphere Entertainment ownership may influence product direction

---

## R&D Relevance to Sonorant

| Criterion | Score (0-10) | Rationale |
|-----------|--------------|-----------|
| HF clarity & transient | 8 | 78 silk dome tweeters individually processed; FPGA-based FIR filtering |
| Directivity control & imaging | 10 | Best-in-class 3D beamforming + WFS; 0.1° resolution; virtual source positioning |
| Sub-weight & infrasonic | 5 | MD80-S reaches 26Hz but 160kg; no standalone infrasonic optimization |
| Psychoacoustic potential | 10 | WFS creates physically reconstructed wavefronts; true spatial perception |
| Small-room viability | 4 | X2 (15.6kg) most viable but 80Hz min; X1 modules far too large; venue-scale focus |

**Composite Score:** 7.73/10

**Key Takeaways for Sonorant:**

1. **WFS Paradigm:** Physical wavefront reconstruction fundamentally different from phantom imaging; worth studying EP3061271B1
2. **Per-Driver Processing:** FPGA-based individual driver control enables capabilities impossible with traditional amplification
3. **Scale Mismatch:** Technology optimized for venue-scale (Sphere) not small-room applications
4. **Virtual Source Positioning:** Psychoacoustically significant capability for immersive experiences
5. **Architecture Insight:** Decentralized processing model maintains computational efficiency regardless of system scale

---

## Sources

1. [HOLOPLOT About Us](https://holoplot.com/about-us)
2. [HOLOPLOT X1 Product Page](https://holoplot.com/products/systems/x1)
3. [HOLOPLOT X2 Product Page](https://www.holoplot.com/products/x2)
4. [audioXpress: R&D Stories — X1 Matrix Array](https://audioxpress.com/article/r-d-stories-design-and-development-of-the-holoplot-x1-matrix-array)
5. [MSG Sphere Case Study](https://www.holoplot.com/case-studies/msg-sphere-case-study)
6. [Illuminarium Atlanta Case Study](https://www.holoplot.com/case-studies/illuminarium-experiences-atlanta-case-study)
7. [Patent EP3061271B1 — Wave Field Synthesis System](https://patents.google.com/patent/EP3061271B1/en)
8. [AREA15 Portal Announcement](https://holoplot.com/insights/news/area15-utilizes-holoplot-x1-to-transport-visitors-through-space-and-time)
9. [Sphere Entertainment Acquires HOLOPLOT (PR Newswire)](https://www.prnewswire.com/news-releases/sphere-entertainment-acquires-holoplot-302143439.html)
10. [TIME: Best Inventions 2022](https://time.com/collection/best-inventions-2022/6229122/holoplot-x1-matrix-array/)

---

## Audit Notes

- **Source Count:** 10 (meets threshold)
- **Independent Measurements:** None found. All specs are manufacturer claims.
- **Patents Verified:** EP3061271B1 confirmed via Google Patents
- **Gaps:** X2 detailed SPL/frequency specifications limited. No small-venue deployment data.
- **Corporate Context:** Sphere Entertainment acquisition (May 2024) may influence future product development toward venue-scale applications.
- **Notable Achievement:** MSG Sphere installation represents world's largest concert sound system (167,000 drivers).
- **last_audited:** 2025-02-05
