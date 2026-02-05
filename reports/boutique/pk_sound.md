# PK Sound — Company Dossier

**Company ID:** `pk_sound`
**Founded:** 2009
**HQ:** Rocky View County (Calgary), Alberta, Canada
**Status:** Active, Private

---

## Company Overview

PK Sound was founded in 2009 by Jeremy Bridge at the foot of the Rocky Mountains in Calgary, Alberta. The company originated as a speaker-rental business Bridge started while in university. The company has since grown into a globally recognized manufacturer of robotic line source systems, headquartered in an expansive facility east of Calgary.

PK Sound's name derives from "Polar Kinetic" — the radial directivity of a loudspeaker resulting from motion.

### Key People

| Name | Role | Notes |
|------|------|-------|
| Jeremy Bridge | CEO, Founder | Started as rental company in university |

---

## Design Philosophy

**Tags:** `robotic_steering`, `variable_directivity`, `line_source`, `mechanical_optimization`, `dsp_integrated`

PK Sound's approach centers on mechanical optimization over DSP-based beam steering. Core principles:

1. **Polar Kinetic Design:** Soundfield shape determined by physical motion, not digital processing
2. **Robotic Precision:** 0.1° vertical resolution, 5° horizontal increments
3. **Mechanical > DSP:** Avoids beam steering that compromises output quality
4. **Real-Time Adjustment:** Coverage modifications after system is flown

### Notable Achievement

> "In 2015, PK Sound patented the world's first robotic line-source system — robotics within the loudspeakers control both vertical and horizontal directivity."
> — Avenue Calgary [1]

---

## Core Technologies

### 1. Robotic Mounting & Adjustment (US20140353074A1)
- **Patent:** US20140353074A1
- **Principle:** Vertical and horizontal angles adjusted remotely via integrated robotic actuators while system is flown
- **Vertical Precision:** 0.1° resolution via linear actuators
- **Duty Cycle:** 80,000+ actuations (109 years theoretical lifecycle)

### 2. Coherent Midrange Integrator (CMI) Waveguide (US9894433B2)
- **Patent:** US9894433B2
- **Principle:** Robotic actuators modify waveguide angle for variable horizontal directivity
- **Design Rules:**
  - Exit apertures ≤ half wavelength of highest frequency
  - Exit angles > 45° to minimize backward energy
  - Transducer distance changes ≤ quarter wavelength
- **Range:** 60°-120° in 5° increments, symmetric and asymmetric

### 3. Kontrol Software
- Remote access to DSP features
- Real-time monitoring
- Multi-axis coverage adjustments after fly

---

## Product Lines

### Trinity Line Source (Robotic)

| Model | Bandwidth | Max SPL | Power | H Coverage | V Coverage | Drivers | Weight |
|-------|-----------|---------|-------|------------|------------|---------|--------|
| **T10** | 40Hz–20kHz | 146 dB | 3000W (4ch Class D) | 60°–120° robotic | 0°–12° (0.1° res) | 2×10" LF, 2×6.5" MF, 1×4" planar HF | 47.6 kg |
| **Trinity Black** | — | — | — | Robotic | Robotic | — | — |

*Spec provenance: Manufacturer. Max SPL with limiters/DSP active.*

**Physical:**
- Dimensions: 980 × 250 × 561 mm (38.6" × 9.8" × 22.1")
- Construction: Void-free Baltic birch
- Max array: 24 modules
- IP Rating: IP69K static, IP66 dynamic

**Robotics:**
- Horizontal thrust: 750 N
- Vertical thrust: 2500 N
- Actuator lifecycle: 80,000 actuations

### Gravity Subwoofers

| Model | Type | Amplification | Drivers | Features |
|-------|------|---------------|---------|----------|
| **G218** | Bass reflex | 8500W Class D IpalMod | 2×18" high-excursion | Cardioid-arrayable, unrestricted vent |
| **T218** | Intelligent sub | — | 2×18" | Trinity integration |

*Spec provenance: Manufacturer. Cardioid capability via array configuration.*

### Tx Series (Intelligent Point Source)

- Point source modules with onboard DSP
- Kontrol software integration

---

## Patents Summary

| Patent | Year | Title | Technology |
|--------|------|-------|------------|
| US20140353074A1 | — | Robotic mounting & adjustment | Vertical angle adjustment via linear actuators |
| US9894433B2 | — | CMI Waveguide | Variable horizontal directivity via robotic actuators |

---

## Case Studies

### Shambhala Music Festival (British Columbia)

- **Type:** Outdoor EDM festival
- **Relationship:** PK Sound "grew out of Shambhala" — founders connected through festival early on
- **System (Village Stage 2022):** Trinity Black + T218 subwoofers
- **Benefit:** Permanent rigging points; serves as proving ground for new technology
- **Software:** .dynamics platform for precise soundfield tailoring, noise bleed minimization
- **Source:** [2]

### EDC Las Vegas 2015 (BassPOD)

- **System:** 16× Trinity modules per side + 69× CX800 dual 18" subs
- **Outcome:** LA Weekly named BassPOD "top pick of the festival"
- **Significance:** Debut success for Trinity system
- **Source:** [3]

### Essence Festival (New Orleans Superdome)

- **System:** Trinity Black
- **Venue:** Indoor stadium
- **Source:** [1]

### Hamilton World Tour

- **Product:** G30 subwoofers
- **Application:** Broadway touring production
- **Source:** [1]

---

## Technical Observations

### Strengths
- **Patented Robotics:** Unique mechanical beam steering avoids DSP compromises
- **Festival-Proven:** Extensive EDM/outdoor festival validation
- **Weather Resistance:** IP69K/IP66 ratings
- **Actuator Durability:** 109-year theoretical lifecycle

### Unique Value Proposition
Unlike DSP-based beam steering (HOLOPLOT, Renkus-Heinz), PK Sound achieves directivity control mechanically, claiming better output quality preservation.

### Data Gaps
- **No Independent Measurements:** No third-party verification of SPL or coverage claims
- **Limited Small-Venue Data:** Primarily large-scale festival/touring applications
- **Subwoofer Specs Incomplete:** G218 frequency response, sensitivity not documented

---

## R&D Relevance to Sonorant

| Criterion | Score (0-10) | Rationale |
|-----------|--------------|-----------|
| HF clarity & transient | 7 | 4" planar wave HF driver; festival-scale optimization |
| Directivity control & imaging | 9 | Patented robotic 3D beam steering; 0.1° precision; mechanical > DSP |
| Sub-weight & infrasonic | 6 | G218 cardioid-capable but no extension specs; festival-scale subs |
| Psychoacoustic potential | 7 | Real-time coverage adjustment; reduced reflections; EDM validation |
| Small-room viability | 3 | Large-format touring/festival focus; T10 at 47.6kg is substantial |

**Composite Score:** 6.79/10

**Key Takeaways for Sonorant:**
1. **Mechanical Beam Steering Patents:** US9894433B2 (CMI Waveguide) worth studying for directivity without DSP compromise
2. **Not Small-Venue Focused:** Products optimized for festival/stadium scale
3. **EDM Validation:** Extensive electronic music festival deployment
4. **IP66/IP69K Ratings:** Weather resistance for outdoor applications
5. **Design Philosophy Contrast:** Mechanical vs. DSP beam steering debate relevant to system architecture decisions

---

## Sources

1. [Avenue Calgary: PK Sound Company Profile](https://www.avenuecalgary.com/city-life/innovation/pk-sound-calgary-audio-technology-company/)
2. [PK Sound: Village Stage Shambhala Case Study](https://pksound.live/application/touring-and-festivals/80-reimagined-village)
3. [Vice: PK Sound Festival Circuit](https://www.vice.com/en/article/from-shambhala-to-edc-pk-sound-is-on-a-never-ending-festival-circuit/)
4. [PK Sound: T10 Product Page](https://pksound.live/product/line-source/t10)
5. [ProSoundWeb: Tech Focus PK Sound Robotic Technology](https://www.prosoundweb.com/tech-focus-pk-sound-robotic-line-array-technology/)
6. [audioXpress: Trinity Black Launch](https://audioxpress.com/news/pk-sound-launches-trinity-black-robotic-line-source-element)
7. [ProSoundWeb: Gravity 218 Launch](https://www.prosoundweb.com/pk-sound-launches-gravity-218-subwoofer/)
8. [FOH Magazine: PK Sound Trinity](https://fohonline.com/articles/product-focus/pk-sound-trinity/)
9. [TPi Magazine: Shambhala 2022](https://www.tpimagazine.com/shambhala-music-festival-returns-with-pk-sound/)
10. [ProSoundWeb: Shambhala Coverage](https://www.prosoundweb.com/pk-sound-covers-british-columbias-shambhala-music-festival/)

---

## Audit Notes

- **Source Count:** 10 (meets threshold)
- **Independent Measurements:** None found. All specs are manufacturer claims.
- **Patents Verified:** Two patents confirmed via Google Patents (US20140353074A1, US9894433B2)
- **Gaps:** G218 subwoofer frequency response and sensitivity not documented. Trinity Black full specs not found. Limited small-venue applications.
- **Provenance:** All specs from manufacturer; no third-party verification.
- **last_audited:** 2025-02-05
