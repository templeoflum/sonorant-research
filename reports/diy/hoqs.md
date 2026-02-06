# HOQS (High Order Quarterwave Society) — Designer Profile

**Designer:** Kaironex (primary designer)
**Location:** Australia
**Website:** https://www.hoqs.com.au
**Store:** https://store.hoqs.com.au
**Active Since:** ~2017
**Last Updated:** 2025-02-06
**Author:** Transducer Archive (CLI agent)

---

## 1. Designer Overview

HOQS (High Order Quarterwave Society) originated as a Facebook group dedicated to compound quarterwave loudspeaker design and evolved into a full design house and driver manufacturer. The primary designer, known as Kaironex, developed the Paraflex loading technology and maintains a comprehensive catalog of subwoofer and mid-top designs.

**Business Model:**
- Open-source plans (free PDF/DXF available for most designs)
- Proprietary driver manufacturing (N-series neodymium, F-series ferrite)
- Global dealer/builder network
- Flat-pack kit distribution through partners (Speaker Hardware, Subcity Audio, etc.)

HOQS has moved from a hobby/community project to a commercial operation with international warehouse stock and authorized dealers on multiple continents.

---

## 2. Design Philosophy

HOQS designs prioritize:

- **Efficiency over box size** — Paraflex cabinets are typically larger than comparable reflex designs but achieve higher sensitivity and output
- **Extended low frequency response** — Type O designs tune to 35Hz; deeper-tuned variants available
- **Compound loading** — Multiple resonators working together for bandwidth extension
- **DIY accessibility** — Plans freely available; CNC-friendly panel designs
- **Driver optimization** — In-house drivers specifically engineered for Paraflex loading

The approach is engineering-first: designs are developed through simulation (Hornresp, Akabak) and validated through measurement before release.

---

## 3. Technology Summary: Paraflex Loading

### What It Is

Paraflex is a compound quarterwave resonator loading technique. Unlike simple bass reflex (one resonator) or transmission line (one path), Paraflex uses two parallel quarterwave resonators that merge into a single exit chamber (mouth).

### How It Works

1. **Low Tuned Resonator (LTR):** A longer path tuned to extend low-frequency response
2. **High Tuned Resonator (HTR):** A shorter path tuned higher for output and cone control
3. **Shared Mouth:** Both resonators terminate at a common exit, summing acoustically

The combination creates a high-pressure zone in front of the HTR chamber that enhances cone control and extends usable bandwidth compared to single-resonator designs.

### Key Benefits

- Higher sensitivity than sealed or ported boxes of similar driver complement
- Extended low-frequency response without the group delay penalty of very low-tuned ports
- Improved transient response compared to ported designs at similar extension
- Reduced port turbulence (no traditional port tube)

### Tradeoffs

- Larger cabinet volume than conventional reflex
- More complex internal construction (multiple chambers, precise path lengths)
- Tuning is fixed — less adjustable than ported designs
- Requires careful attention to internal damping and chamber alignment

---

## 4. Product Catalog

### Subwoofers — Type O Series (35Hz Tuning)

| Model | Config | Dimensions (LxWxH mm) | Weight (kg) | Volume (L) | Fb (Hz) | Range (Hz) | Sensitivity | Max SPL | Drivers |
|-------|--------|----------------------|-------------|------------|---------|------------|-------------|---------|---------|
| Type O 2x18 CRAM | 2×18" | 1250×950×610 | 81.5 | 724 | 35 | 35–100 | 104.5 dB | 140/146 dB | N185C, F185C |
| Type O 2x18 Reversed | 2×18" | 1256×918×610 | 81.5 | 703 | 35 | 35–100 | 104.5 dB | 140/146 dB | N185C, F185C |
| Type O 1x18 | 1×18" | ~1070×700×600 | ~50 | ~400 | 35 | 35–100 | ~101 dB | ~137/143 dB | N185C, F185C |
| Type O 1x21 | 1×21" | not established | not established | not established | 35 | 35–100 | not established | not established | N216C |
| Type O 2x12 CRAM | 2×12" | 1000×687×368 | 37 | 253 | 35 | 35–100 | ~98 dB | ~134/140 dB | N124C |

**Notes:**
- "CRAM" = Compact Resonator Array Module — dual-driver versions
- Reversed driver variant places drivers on opposite side for different stacking options
- Sensitivity measured with HOQS drivers in half-space @ 1m

### Subwoofers — Type C Series ("Classic")

| Model | Config | Dimensions (LxWxH mm) | Weight (kg) | Volume (L) | Fb (Hz) | Range (Hz) | Sensitivity | Max SPL | Drivers |
|-------|--------|----------------------|-------------|------------|---------|------------|-------------|---------|---------|
| Type C Classic 1x18 V1 | 1×18" | 915×915×610 | 66.6 | 510 | ~38 | 38–120 | not established | not established | N185C, F185C |
| Type C Classic 1x21 V1 | 1×21" | 915×915×610 | 66.6 | 510 | ~35 | 35–120 | not established | not established | N216C |
| Type C 2x15 CRAM | 2×15" | not established | not established | not established | ~40 | 40–120 | not established | not established | 15" compatible |

**Notes:**
- V2 versions available with refinements
- Type C has split-symmetrical paths for a more traditional folded-horn appearance

### Subwoofers — Type R Series

| Model | Config | Dimensions (LxWxH mm) | Weight (kg) | Volume (L) | Fb (Hz) | Range (Hz) | Sensitivity | Max SPL | Drivers |
|-------|--------|----------------------|-------------|------------|---------|------------|-------------|---------|---------|
| Type R 1x21 | 1×21" | 1200×800×600 | not established | not established | 30 | 30–180 | 104 dB | 137/143 dB | N216C |
| Type R 1x18 | 1×18" | 1070×700×600 | not established | not established | 32 | 32–180 | ~101 dB | ~134/140 dB | N185C, F185C |
| Type R 121 | 1×12" | not established | not established | not established | ~40 | 40–180 | not established | not established | N124C |

**Notes:**
- Type R = optimized for relatively straightforward construction
- Extended operating range compared to Type O (usable higher)

### Subwoofers — ELF / C2E Series

| Model | Config | Dimensions (LxWxH mm) | Weight (kg) | Volume (L) | Fb (Hz) | Range (Hz) | Sensitivity | Max SPL | Drivers |
|-------|--------|----------------------|-------------|------------|---------|------------|-------------|---------|---------|
| C2E ELF | 1×18" | not established | not established | not established | ~28 | 28–80 | not established | not established | N185C |

**Notes:**
- ELF = Extended Low Frequency — deeper tuning for infrasonic extension
- Designed for stacking with higher-tuned subs for full-range coverage

### Mid-Tops / Kick-Tops

| Model | Config | Dimensions (mm) | Weight (kg) | Volume (L) | Range (Hz) | Sensitivity | Max SPL | Drivers |
|-------|--------|-----------------|-------------|------------|------------|-------------|---------|---------|
| 2x8 Mid-Top | 2×8" | 600(f)×383(r)×615×508 | not established | not established | 150–3000 | not established | not established | 8" compatible |
| G1V2 1x12 Kick-Top | 1×12" | 600×600×360 | 21.8 | 130 | 80–800 | not established | not established | 12" compatible |
| C3DKT 1x12 Kick-Top | 1×12" (trapezoid) | 615×600(f)/383(r)×508 | 21.5 | 150 | 80–800 | not established | not established | 12" compatible |
| WSV2 2x12 | 2×12" | not established | not established | not established | 60–800 | not established | not established | 12" compatible |

**Notes:**
- Kick-tops designed to run 80–800Hz band between subs and HF
- G1V2 = simpler rectangular box; C3DKT = trapezoid for array curvature
- WSV2 = Wide Style V2, larger format

### Plan Availability

All designs have free PDF plans available through:
- HOQS website (https://www.hoqs.com.au/projects)
- GitHub (High-Order-Quarterwave-Society organization)
- Authorized dealers (Subcity Audio, Speaker Hardware, The Sound Guy ZA)

DXF files for CNC cutting typically included or available on request.

---

## 5. Driver Lineup

HOQS manufactures their own drivers optimized for Paraflex loading.

### Low Frequency Drivers

| Model | Size | Xmax | Power (AES/Program) | Impedance | Sensitivity | BL | Vas | Coil | Cone |
|-------|------|------|---------------------|-----------|-------------|----|----|------|------|
| N185C | 18" | 13.5mm | 1700W / 3400W | 8Ω | not established | 39 | 242L | 125mm (5") Cu | Carbon fiber |
| N216C | 21" | not established | not established | 8Ω | not established | not established | not established | 150mm (6") Cu | Carbon fiber |
| F185C | 18" | not established | 1200W / 2400W | 8Ω | not established | not established | not established | not established | not established |
| N124C | 12" | not established | not established | 8Ω | not established | not established | not established | not established | Carbon fiber |

**Notes:**
- N-series = Neodymium motor
- F-series = Ferrite motor (lower cost, heavier)
- Motors designed with Finite Element Analysis (FEA)
- Carbon fiber cones for stiffness and low mass

### Pricing (approximate, varies by region)

- N185C: ~$500–600 USD
- N216C: ~$700–800 USD
- F185C: ~$350–450 USD

---

## 6. Build Requirements

### Materials

- **Plywood:** 18mm Baltic Birch recommended; 15mm acceptable for some designs
- **Bracing:** Internal bracing specified in plans
- **Damping:** Acoustic foam or polyfill in specified locations
- **Hardware:** T-nuts, handles, corners, speakON connectors

### Tools

- **CNC recommended:** Complex internal geometry benefits from CNC precision
- **Hand-build possible:** With careful measurement and jigsaw/router work
- **Minimum tools:** Circular saw, jigsaw, router, drill, clamps

### 3D Printed Components

Not required for most designs. Some builders use 3D-printed port flares or driver adapters.

### Assembly Complexity

| Design | Complexity |
|--------|------------|
| Type R | Intermediate — relatively straightforward construction |
| Type O | Intermediate-Advanced — more complex internal paths |
| Type C | Intermediate — split-symmetrical paths |
| Mid-Tops | Beginner-Intermediate — simpler geometry |

---

## 7. DSP/Processing Requirements

### Active Crossover

All HOQS systems run active crossover:
- **Subs:** HPF at Fb (35Hz for Type O), LPF typically 80–120Hz
- **Kick-tops:** BPF 80–800Hz typical
- **HF:** Added separately (horn or direct radiator)

### Processing Platforms (Community Usage)

- miniDSP (2x4 HD, SHD series)
- Behringer DCX2496 / DriveRack
- QSC Q-Sys (larger deployments)
- Lake / Linea Research (professional)
- Pure Data patches available for software DSP

### FIR Filters

Community-developed FIR presets exist but are not officially provided by HOQS. Most users run IIR crossovers with parametric EQ.

### Amplification

- **Per 2×18 sub:** 2000–4000W RMS recommended
- **Per kick-top:** 500–1000W RMS recommended
- Popular choices: Crown XLS, Powersoft, Lab Gruppen, QSC PLX/PLD

---

## 8. Community Track Record

### Build Threads

- diyAudio: Extensive "Compound loading 6th order quarterwave" thread (300+ pages)
- Facebook: HOQS group (primary community hub)
- GitHub: High-Order-Quarterwave-Society organization with plans and documentation

### Number of Builds

Estimated hundreds worldwide across all designs. Type O 2×18 and Type C Classic are the most popular sub designs.

### Reported Issues

- **Path length precision:** Critical for proper tuning; small errors affect performance
- **Internal damping:** Insufficient damping causes resonance issues
- **Driver matching:** Non-HOQS drivers require careful T/S matching

### User Impressions

Consistent praise for:
- Low-frequency extension and impact ("hits hard below 40Hz")
- Efficiency and output relative to box size
- Clean transients compared to ported designs

Common critiques:
- Cabinet size (larger than comparable reflex)
- Construction complexity
- Limited adjustment after build

### Notable Deployments

- Festival sound systems (Australia, Europe, Africa)
- Underground/DIY party circuits
- Commercial rental fleets (authorized builders)

---

## 9. Mark I Suitability Assessment

### Type O 2×18 (Builder's Primary Recommendation)

| Criterion | Assessment | Notes |
|-----------|------------|-------|
| 100–200 person venue | **Excellent** | 140dB continuous is far more than needed; single pair sufficient |
| Sub-bass weight | **Excellent** | 35Hz tuning with strong output; "felt" bass achieved |
| Infrasonic extension | **Good** | 35Hz Fb limits true infrasonic (<20Hz) response; ELF variant extends lower |
| Hyper-real clarity | N/A | Sub-only; depends on paired tops |
| Fast transients | **Very Good** | Paraflex loading provides better transients than deep-tuned ported |
| Small-room optimization | **Good** | Omnidirectional bass; no cardioid option but manageable in small rooms |
| Transportability | **Fair** | 81.5kg unloaded + drivers is heavy; requires two-person lift and truck |
| Builder availability | **Excellent** | Authorized HOQS dealer available; full support ecosystem |

### Alternative Options

**Type O 1×18:** Lighter (~50kg), still substantial output, easier to transport. Recommended if transportability is prioritized over maximum output.

**Type R 1×21:** Deeper tuning (30Hz), extended range, but larger cabinet. Good for infrasonic emphasis.

**Type O 2×12 CRAM:** Much lighter (37kg), easier to handle, but less low-end weight. Better for smaller venues or as supplement.

### Pairing Recommendation

Type O 2×18 + G1V2 or C3DKT kick-tops + separate HF (horn or coaxial) creates a full 3-way system. The builder can advise on specific HF options.

---

## 10. Sources

1. HOQS Australia website — https://www.hoqs.com.au [designer-published]
2. HOQS Store — https://store.hoqs.com.au [designer-published]
3. HOQS GitHub — https://github.com/High-Order-Quarterwave-Society [designer-published]
4. Subcity Audio HOQS page — https://www.subcityaudio.com/hoqsplans [industry]
5. Speaker Hardware Paraflex kits — https://www.speakerhardware.com [industry]
6. The Sound Guy ZA HOQS distributor — https://www.thesoundguy.co.za/HOQS-Paraflex [industry]
7. diyAudio "Compound loading 6th order quarterwave" thread — https://www.diyaudio.com/community/threads/309352/ [community-measured]
8. WAAT Audio product listings — https://waataudio.com [industry]

---

## 11. Open Questions

- **Infrasonic extension:** Type O tunes to 35Hz. For true sub-30Hz "chest pressure," is the ELF variant or different design needed?
- **Weight tolerance:** 81.5kg is heavy. Is the 1×18 variant acceptable output for Mark I scale?
- **HF pairing:** What HF solution does the builder recommend to complete the system?
- **DSP preset:** Does the builder provide tuned DSP presets, or is system tuning part of the build process?
- **Lead time:** What is current delivery timeline for drivers and flat-packs?
