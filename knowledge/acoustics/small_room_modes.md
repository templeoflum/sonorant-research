# Small-Room Modal Behavior and Treatment

**Status:** draft
**Confidence:** high
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Sources

1. Everest, F.A. & Pohlmann, K.C. (2015). *Master Handbook of Acoustics*, 6th Edition. McGraw-Hill. [textbook]
2. Toole, F.E. (2018). *Sound Reproduction: The Acoustics and Psychoacoustics of Loudspeakers and Rooms*, 3rd Edition. Routledge. [textbook]
3. Schroeder, M.R. (1996). "The 'Schroeder frequency' revisited." *Journal of the Acoustical Society of America*, 99(5), 3240-3241. [peer-reviewed]
4. Sonarworks. "Mastering Room Acoustics: Conquer Room Modes." https://www.sonarworks.com/blog/learn/room-modes [industry]
5. ProSoundTraining. "Divide and Conquer - The Schroeder Frequency." https://www.prosoundtraining.com/2021/10/14/divide-and-conquer-the-schroeder-frequency/ [industry]

## Summary

Room modes are resonant frequencies at which sound waves form standing wave patterns between parallel surfaces. In small rooms typical of 100–200 cap venues, these modes occur at bass frequencies where they significantly affect perceived tonal balance and decay characteristics. Understanding modal behavior is essential for system tuning and placement strategy in any Sonorant deployment.

## Detail

### Types of Room Modes

Rectangular rooms have three types of resonant modes [1]:

**Axial modes:** Waves reflecting between two parallel surfaces (e.g., front-to-back wall). These are the strongest modes, with the most impact on bass response.

**Tangential modes:** Waves reflecting between two pairs of parallel surfaces (e.g., bouncing off all four walls but not floor/ceiling). These have half the intensity of axial modes.

**Oblique modes:** Waves reflecting between all three pairs of parallel surfaces. These have one-quarter the intensity of axial modes and are numerous but individually weak.

### Calculating Room Modes

For a rectangular room with dimensions L (length), W (width), and H (height) in meters, axial mode frequencies are:

```
f = (c/2) × √[(p/L)² + (q/W)² + (r/H)²]
```

Where:
- c = speed of sound (~343 m/s at 20°C)
- p, q, r = mode indices (0, 1, 2, 3...)
- For axial modes: only one index is non-zero
- For tangential: two indices are non-zero
- For oblique: all three indices are non-zero

**Simplified axial mode formula:**
```
f = c/(2L) × n  where n = 1, 2, 3...
```

For a 10m room: first axial mode = 343/(2×10) = 17.2 Hz

### The Schroeder Frequency

The Schroeder frequency marks the transition between the modal region (distinct resonances) and the statistical region (dense, overlapping modes that behave more uniformly) [3]:

```
f_s = 2000 × √(T60/V)
```

Where:
- T60 = reverberation time in seconds
- V = room volume in cubic meters
- f_s = Schroeder frequency in Hz

**Typical values:**
- Small control room (50 m³, T60=0.3s): f_s ≈ 155 Hz
- Medium venue (300 m³, T60=0.5s): f_s ≈ 82 Hz
- Large hall (5000 m³, T60=1.5s): f_s ≈ 35 Hz

Below the Schroeder frequency, room behavior is dominated by individual modes that must be addressed specifically. Above it, modes overlap sufficiently that treatment can be more general.

### Modal Problems in Small Rooms

Small rooms have several modal challenges [2][4]:

**Wide mode spacing:** In small rooms, modes are spaced farther apart in frequency, creating audible peaks and dips rather than smooth response.

**Bass buildup at boundaries:** Sound pressure is maximum at room boundaries (walls, floor, ceiling) for all modes. Corners, where three boundaries meet, have the highest bass buildup.

**Null patterns:** Between pressure maxima, there are pressure minima (nulls) where bass cancels. A listener at a null position hears dramatically reduced bass at that frequency.

**Decay time variation:** Different modes decay at different rates depending on surface absorption at reflection points. Some modes "ring" much longer than others.

### 100–200 Cap Venue Characteristics

Venues typical of Sonorant's target scale might have dimensions like:

| Room size | Dimensions (L×W×H) | First axial modes |
|-----------|-------------------|-------------------|
| Small bar | 8×6×3 m | 21, 29, 57 Hz |
| Medium club | 12×10×4 m | 14, 17, 43 Hz |
| Warehouse | 20×15×5 m | 9, 11, 34 Hz |

The first axial modes fall directly in the critical sub-bass range. These will dominate the room's bass character.

### Treatment Approaches

**Bass traps (absorption):**
- Most effective in corners where pressure is maximum
- Membrane/panel absorbers tuned to problem frequencies
- Porous absorbers (thick) for broadband absorption
- Trade-off: reducing modal energy also reduces overall bass level

**Diffusion:**
- Breaks up standing wave patterns
- Less effective at low frequencies (requires large structures)
- Better suited to mid-frequencies and above

**Speaker and listener placement:**
- Avoid placing speakers or listeners at mode nulls
- Placing subs in corners excites all modes maximally (high output but modal emphasis)
- Distributed sub placement (multiple positions) can smooth modal response

**DSP correction:**
- Room EQ can reduce modal peaks but cannot fill nulls
- Parametric EQ to notch specific problem modes
- Cannot fix position-dependent variations

### The Multiple-Subwoofer Approach

Research (Toole, Welti) shows that multiple subwoofers in optimized positions can dramatically smooth modal response [2]:

- **1 sub:** Highly position-dependent, strong modal variation
- **2 subs (opposite walls):** Cancels some axial modes
- **4 subs (midpoints of each wall):** Further smoothing
- **Asymmetric placement:** Can be optimized for specific room geometries

This approach trades hardware cost for acoustic performance.

## Relevance to Sonorant

Every Sonorant deployment will be in a different small room. Modal behavior is the dominant acoustic challenge:

1. **Variable response:** The same system will sound different in every room below the Schroeder frequency. Tuning cannot be "set and forget" — each venue requires assessment.

2. **Sub placement:** "Optimal" sub position varies by room. A portable system needs placement flexibility and measurement capability to find good positions quickly.

3. **Treatment limitations:** Unlike a fixed installation, Sonorant cannot rely on permanent room treatment. Portable bass traps could help but add transport burden.

4. **DSP as primary tool:** Room EQ becomes essential for consistent sub-80 Hz performance across venues. This has implications for the signal chain design.

5. **Expectation management:** Perfect bass response in arbitrary small rooms is not achievable. The goal should be "good enough" smoothness with minimal position-dependent variation.

6. **Potential multiple-sub benefit:** A modular system with multiple small subs (rather than one large sub) could exploit distributed placement for modal smoothing.

## Open Questions

- What measurement/analysis workflow should Sonorant use for venue assessment before each deployment?
- Is a dual-sub (or quad-sub) configuration worth the complexity for modal smoothing benefits?
- What room size range (min/max) represents realistic Sonorant venues, and what are the modal characteristics of that range?
- Can predictive modeling (input room dimensions, output optimal sub positions) be practical for rapid deployment?
