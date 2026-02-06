# JW Sound (John White) — Designer Profile

**Designer:** John White
**Location:** United States
**Website:** https://www.jwsound.live
**Active Since:** ~2018 (MEH designs)
**Last Updated:** 2025-02-06
**Author:** Transducer Archive (CLI agent)

---

## 1. Designer Overview

JW Sound is the design portfolio of John White, focused on Multiple Entry Horn (MEH) loudspeakers in the Danley Synergy Horn lineage. The flagship JMOD design has become one of the most popular DIY MEH implementations, with active community build threads on diyAudio and AVS Forum.

**Business Model:**
- Free DIY plans (PDF) for personal use
- Optional donations accepted
- Store with 3D-printed components and flatpacks (https://www.jwsound.live/store)
- No driver manufacturing — designs use commercial drivers (B&C, 18 Sound, etc.)

JW Sound also hosts Josh Ricci's subwoofer designs (SKHORN, SKRAM) on the website, creating a one-stop resource for DIY high-performance sound systems.

---

## 2. Design Philosophy

JW Sound designs prioritize:

- **Point-source coherence** — All drivers sum acoustically through a shared horn mouth, eliminating comb filtering between drivers
- **Pinpoint imaging** — MEH geometry creates a single acoustic center for precise soundstage
- **High output** — Horn loading provides efficiency and SPL capability
- **Controlled directivity** — Defined coverage patterns (90×60° for JMOD)
- **DIY accessibility** — CNC-cuttable panels with 3D-printed transition components

The approach inherits from Tom Danley's Synergy Horn work and Scott Hinson's "Ultimate Loudspeaker" DIY adaptation, bringing MEH technology to the home builder at manageable complexity.

---

## 3. Technology Summary: Multiple Entry Horn (MEH)

### What It Is

A Multiple Entry Horn (MEH) is a loudspeaker where multiple drivers (woofers, midranges, compression driver) all fire into a shared horn, with their outputs acoustically summing at a common point. This differs from conventional multi-way speakers where each driver has its own exit point.

### How It Works

1. **Shared horn mouth:** All drivers couple into a single expanding horn
2. **Staggered entry points:** Each driver enters the horn at a different position based on its frequency range
3. **Acoustic summation:** Sound waves from all drivers combine at the horn mouth
4. **Time alignment:** Physical placement and DSP ensure all drivers arrive in phase at the listening position

The result is a speaker that behaves as a point source across its entire bandwidth — the imaging and phase coherence of a full-range driver with the output and extension of a multi-way system.

### Key Benefits

- **Coherent imaging:** No comb filtering between drivers; sounds like a single source
- **Controlled directivity:** Horn loading provides consistent coverage pattern
- **High efficiency:** Horn loading converts amplifier power to SPL efficiently
- **Dynamic punch:** Horn speakers have characteristic dynamic impact

### Lineage

- **Danley Synergy Horn:** Original commercial implementation (Tom Danley patents)
- **Scott Hinson:** "The Ultimate Loudspeaker" essay brought MEH to DIY
- **JMOD/JW Sound:** Modern DIY refinement with 3D-printed components

---

## 4. Product Catalog

### JMOD (Primary Design)

| Spec | JMOD v1 | JMOD v2 |
|------|---------|---------|
| Configuration | 2×12" woofer + compression driver | 2×12" woofer + coaxial compression driver |
| Coverage | 90° × 60° | 90° × 60° |
| Operating range | 80 Hz – 18 kHz | 80 Hz – 18 kHz |
| LF drivers | B&C 12NDL76 or 12NDL88 | B&C 12NDL76 or 12NDL88 |
| HF driver | B&C DCX464 | B&C DCX464 |
| Crossover | 3-way active: 80Hz / 370Hz / 3500Hz | 3-way active: 80Hz / 370Hz / 3500Hz |
| Sensitivity | ~105 dB (system) | ~105 dB (system) |
| Max SPL | ~130 dB | ~130 dB |
| Dimensions | not established | not established |
| Weight | not established | not established |
| Plan availability | Free PDF | Free PDF |

**Notes:**
- JMOD runs down to 80Hz — requires subwoofer for full-range
- V2 includes refinements based on community feedback
- 3D-printed mouth adaptor required for horn geometry
- Plans available at https://www.jwsound.live/designs/jmod

**Driver Options:**

| Position | Primary | Alternative |
|----------|---------|-------------|
| LF (×2) | B&C 12NDL76 | B&C 12NDL88, 18Sound 12NTLW3500 |
| HF | B&C DCX464 (coaxial) | — |

The 12NDL88 offers slightly extended midrange compared to 12NDL76.

### JMOD-M (Medium Format Array)

| Spec | Value |
|------|-------|
| Configuration | Arrayed module, diamond footprint |
| Dimensions | 1450mm × 630mm × 730mm |
| Volume | 2.25× larger than JMOD 2.0 |
| Use case | Larger venues, line array-style deployment |
| Plan availability | not established |

**Notes:**
- Designed for stacking/arraying multiple units
- Diamond footprint allows tight packing
- Significantly larger than standard JMOD

### Solana (Compact MEH)

| Spec | Value |
|------|-------|
| Configuration | Compact multiple entry waveguide |
| Dimensions | 400mm × 400mm × 320mm |
| Weight | 12.7 kg |
| Construction | 12mm Baltic Birch, composite resin waveguide |
| Mount | 35mm pole / M20 threaded combo |
| Use case | Nearfield monitoring, small PA, fill speakers |
| DSP requirement | FIR filtering for flat amplitude and phase |
| Plan availability | Free PDF (https://www.jwsound.live/solana-diy) |

**Notes:**
- Smallest JW Sound MEH design
- Prioritizes smooth directivity and coherent driver integration
- Highly revealing sonic character for critical listening
- Requires DSP/FIR for optimal performance

### SAWMOD (Shared Aperture Waveguide Module)

| Spec | Value |
|------|-------|
| Configuration | 1" compression driver + 2× mid drivers (4"/5"/6.5" options) + 2×10" rear-firing |
| Dimensions | 115mm × 260mm × 360mm (waveguide module) |
| Operating range | 350 Hz – 20 kHz (waveguide), with LF section to ~80 Hz |
| Crossover | HF: 1200–1300 Hz HP, MF: 350 Hz HP / 1200 Hz LP |
| Use case | Compact high-output module |
| Plan availability | Free PDF |

**Notes:**
- Not strictly an MEH but uses shared aperture principles
- Extremely compact for output capability
- LF section uses rear-firing slotloaded 10" drivers
- Profile refined in Ath4 software

### Ricci Designs (Hosted on JW Sound)

JW Sound hosts Josh Ricci's subwoofer designs:

| Design | Configuration | Type | Notes |
|--------|---------------|------|-------|
| SKRAM | 2×15"–21" | 6th order bandpass | Compact, high efficiency, ~30 Hz extension |
| SKHORN | 2×15"–21" | Quasi tapped horn | Higher output, larger cabinet |

These pair naturally with JMOD for complete systems. See `knowledge/enclosures/tapped_horn.md` for detailed SKHORN/SKRAM analysis.

---

## 5. Driver Lineup

JW Sound does not manufacture drivers. Designs specify commercial drivers:

### Recommended LF Drivers

| Model | Manufacturer | Size | Power | Sensitivity | Notes |
|-------|--------------|------|-------|-------------|-------|
| 12NDL76 | B&C | 12" | 700W AES | 98 dB | Standard JMOD woofer |
| 12NDL88 | B&C | 12" | 800W AES | 98 dB | Extended midrange variant |
| 12NTLW3500 | 18 Sound | 12" | 700W AES | 97 dB | Alternative (untested in JMOD) |

### Recommended HF Drivers

| Model | Manufacturer | Type | Sensitivity | Crossover | Notes |
|-------|--------------|------|-------------|-----------|-------|
| DCX464 | B&C | 1.4" coaxial | 111 dB | 300 Hz min | Primary JMOD compression driver |

---

## 6. Build Requirements

### Materials

- **Plywood:** 18mm Baltic Birch for cabinet panels
- **Horn flares:** 18mm (can bond 6mm layers to existing panels)
- **Waveguide:** 3D-printed (JMOD) or composite resin (Solana)
- **Hardware:** T-nuts, handles, speakON connectors

### Tools

- **CNC strongly recommended:** Complex horn geometry and angled cuts
- **3D printer required:** Mouth adaptor for JMOD
- **Hand-build possible:** With careful jigsaw/router work, but challenging

### 3D Printed Components

| Design | Component | Material |
|--------|-----------|----------|
| JMOD | Mouth adaptor | PLA/PETG |
| Solana | Waveguide option | Composite resin preferred |

### Assembly Complexity

| Design | Complexity | Notes |
|--------|------------|-------|
| JMOD | Advanced | Complex horn geometry, 3D-printed parts, precise alignment |
| Solana | Intermediate | Smaller, but waveguide construction is critical |
| SAWMOD | Advanced | Multiple driver positions, rear-firing LF section |

---

## 7. DSP/Processing Requirements

### Active Crossover (Required)

JMOD is a 3-way active design requiring per-driver amplification:

| Band | Crossover | Driver |
|------|-----------|--------|
| Sub | Below 80 Hz | External subwoofer |
| LF | 80–370 Hz | 2× 12" woofers (parallel) |
| HF | 370–3500 Hz | DCX464 MF section |
| VHF | 3500 Hz+ | DCX464 HF section |

### FIR Filter Design

- **FIR Designer:** Primary tool for creating optimization filters
- **SMAART:** Measurement platform for filter development
- **Custom per-system:** Filters tuned for specific driver/amplifier combinations

### Processing Platforms (Community Usage)

| Platform | Notes |
|----------|-------|
| Linea Research | High-end, used by JW Sound himself |
| QSC Q-Sys | Professional, network-based |
| Hypex FA253 | Plate amplifier with DSP |
| miniDSP | Budget option, requires external amps |

### Amplification

- **Per JMOD:** 3 amp channels (LF, HF, VHF) or 2 if VHF/HF share
- **Recommended power:** 500W+ per LF channel, 200W+ per HF channel
- **Professional choices:** Crown, Powersoft, QSC, Lab Gruppen

---

## 8. Community Track Record

### Build Threads

- **diyAudio:** "JMOD v2 build thread" — active, 50+ pages
- **AVS Forum:** "Multiple Entry Horn" thread — 300+ pages, covers MEH broadly including JMOD
- **Audio Abattoir:** MEH DIY build discussions

### Number of Builds

Estimated 50–100+ JMOD builds worldwide. Active community with ongoing new builds.

### Reported Issues

- **3D print quality:** Mouth adaptor requires good print quality for acoustic seal
- **Driver alignment:** Physical positioning critical for MEH summation
- **DSP complexity:** FIR filter design is non-trivial; not plug-and-play
- **File format issues:** DXF files sometimes need conversion for specific CNC software

### User Impressions

Consistent praise for:
- "Pinpoint imaging" — sounds like a single point source
- "Dynamic punch" — horn character without harshness
- "Coherent soundstage" — instruments have natural placement
- "Low distortion transparency" — compared favorably to ESL/ribbons

Common observations:
- Requires good DSP/measurement skills to optimize
- 80 Hz low-end limit means subwoofer is mandatory
- Build complexity is higher than typical DIY speakers

### Notable Deployments

- Home theater reference systems
- Small venue PA installations
- DJ/electronic music playback systems
- Recording studio monitoring (Solana)

---

## 9. Mark I Suitability Assessment

### JMOD as Mark I Tops (Paired with HOQS Type O Subs)

| Criterion | Assessment | Notes |
|-----------|------------|-------|
| 100–200 person venue | **Excellent** | ~130 dB peak capability far exceeds venue needs |
| Sub-bass weight | **N/A** | Requires subwoofer; pairs with HOQS Type O |
| Hyper-real clarity | **Excellent** | MEH coherence delivers exceptional clarity and detail |
| Fast transients | **Excellent** | Horn loading provides dynamic punch and transient speed |
| Small-room optimization | **Very Good** | Controlled 90×60° directivity helps manage reflections |
| Transportability | **Good** | Size/weight not established but likely <30kg per unit |
| Builder availability | **Fair** | DIY build or find local CNC/3D print services; no dealer network |

### Pairing Analysis: JMOD + HOQS Type O

| Aspect | Assessment |
|--------|------------|
| Frequency handoff | JMOD runs to 80 Hz; Type O tunes to 35 Hz — seamless crossover region |
| Output matching | Both designs have high sensitivity/output — well matched |
| Philosophy alignment | Both prioritize coherence and transient response |
| Build complexity | High — requires CNC, 3D printing, DSP expertise |
| Support ecosystem | HOQS has dealer support; JMOD is community-supported DIY |

### Alternative Top Options

**Solana:** Much smaller, easier to build, but less output. Better for nearfield/smaller venues.

**SAWMOD:** Compact, high-output, but still in development with less community track record.

**HOQS Mid-Tops:** G1V2 or C3DKT are simpler to build and pair naturally with HOQS subs, but don't offer MEH coherence.

---

## 10. Sources

1. JW Sound designs page — https://www.jwsound.live/designs [designer-published]
2. JW Sound JMOD page — https://www.jwsound.live/designs/jmod [designer-published]
3. JW Sound Solana page — https://www.jwsound.live/designs/solana [designer-published]
4. JW Sound JMOD-M page — https://www.jwsound.live/designs/jmodm-medium-format-array [designer-published]
5. diyAudio JMOD v2 build thread — https://www.diyaudio.com/community/threads/jmod-v2-build-thread.429672/ [community-measured]
6. AVS Forum MEH thread — https://www.avsforum.com/threads/multiple-entry-horn.3315550/ [community-measured]
7. diyAudio SAWMOD thread — https://www.diyaudio.com/community/threads/saw-module-project-thread.435033/ [community-measured]
8. B&C Speakers datasheets — https://www.bcspeakers.com [industry]

---

## 11. Open Questions

- **JMOD v2 availability:** Are v2 plans finalized and released? What are the specific improvements over v1?
- **Cabinet dimensions:** Exact LxWxH for JMOD not established in available sources
- **Weight:** Unloaded cabinet weight not established
- **3D print source:** Does JW Sound sell pre-printed mouth adaptors, or is DIY printing required?
- **DSP presets:** Are there community-shared FIR presets, or must each builder develop their own?
- **Build timeline:** How long does a typical JMOD build take for a first-time builder with CNC access?
- **Driver sourcing:** Are B&C 12NDL76 and DCX464 readily available, or subject to supply chain issues?
