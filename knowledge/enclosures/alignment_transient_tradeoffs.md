# Sealed vs. Ported vs. Horn — Transient Response Tradeoffs

**Status:** draft
**Confidence:** high
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Sources

1. Small, R.H. (1972). "Closed-Box Loudspeaker Systems Part I: Analysis." *Journal of the Audio Engineering Society*, 20(10), 798-808. [peer-reviewed]
2. Thiele, A.N. (1971). "Loudspeakers in Vented Boxes: Part I." *Journal of the Audio Engineering Society*, 19(5), 382-392. [peer-reviewed]
3. Dickason, V. (2006). *Loudspeaker Design Cookbook*, 7th Edition. Audio Amateur Press. [textbook]
4. Audioholics. "Sealed vs Ported Subwoofers: Which Is Right For You?" https://www.audioholics.com/loudspeaker-design/sealed-vs-ported-subwoofers [industry]
5. Ricci, J. "Group Delay and Transient Response Comparisons." Data-Bass.com measurements. [community]

## Summary

The three major enclosure alignments — sealed (acoustic suspension), ported (bass reflex), and horn-loaded — exhibit fundamentally different transient response characteristics due to their filter topologies. Sealed boxes offer the best transient response (lowest group delay, fastest impulse decay) at the cost of efficiency and extension. Ported boxes extend lower and louder but ring longer. Horns can achieve excellent transient response above their cutoff frequency but require large size for deep bass.

## Detail

### Filter Topology Differences

**Sealed enclosure:** Behaves as a second-order (12 dB/octave) high-pass filter [1]. The system Q (Qtc) determines both frequency response shape and transient behavior. Lower Q = more damped response = better transients but earlier rolloff.

**Ported enclosure:** Behaves as a fourth-order (24 dB/octave) high-pass filter [2]. The higher-order filter extends bass response lower but introduces more phase shift and group delay in the passband. The port resonance creates additional energy storage that affects decay time.

**Horn-loaded:** Not a simple filter topology; depends heavily on horn geometry. Above the horn cutoff frequency, the driver operates into a resistive load with excellent damping. Below cutoff, the horn unloads and response drops rapidly.

### Group Delay Characteristics

Group delay measures how much different frequencies are delayed relative to each other — higher group delay means bass frequencies arrive later than midrange, smearing transients.

**Typical values [4][5]:**

| Alignment | Group delay at tuning frequency |
|-----------|--------------------------------|
| Sealed (Qtc=0.7) | ~5 ms |
| Well-designed ported | ~15 ms |
| Poorly designed ported | 25+ ms |
| Horn (above cutoff) | Very low |

The sealed box cone starts and stops more quickly and more cleanly [4]. Ported boxes have more complicated transient response with more "ringing" due to the resonant port interaction.

### Impulse Response Differences

**Sealed:** Clean initial transient with exponential decay determined by system Q. Higher Qtc gives more output near resonance but slower decay; lower Qtc gives faster decay but less extension.

**Ported:** Initial transient followed by extended ringing as energy stored in the port resonance dissipates. The impulse response shows multiple cycles of decay. This manifests as "one-note bass" when poorly tuned.

**Horn:** Above cutoff, the horn provides resistive loading that damps the driver very effectively. Impulse response can be excellent. Below cutoff, the horn unloads and driver behavior reverts to its free-air (uncontrolled) characteristics.

### The Relationship Between Q and Transients

System Q (Qtc for sealed, Qts/box tuning for ported) directly affects transient behavior:

- **Q = 0.5 (critically damped):** No overshoot, fastest settling, but -6dB at resonance
- **Q = 0.707 (Butterworth):** Maximally flat frequency response, slight overshoot, good transients
- **Q > 1.0 (underdamped):** Peaked response, significant ringing, poor transients

Most sealed designs target Qtc = 0.707 as a balance. Higher-output sealed designs push Qtc to 1.0+, sacrificing transient response for sensitivity.

Ported designs inherently have more energy storage regardless of alignment because the port itself resonates. However, careful alignment can minimize ringing — the best ported designs can approach sealed transient quality while extending response lower.

### Measured Examples

Data-Bass.com measurements (Ricci) show:

- **Sealed subs (well-designed):** Group delay under 10ms across the passband, clean waterfall decay
- **Ported subs (well-designed):** Group delay 10–20ms, modest ringing visible in waterfall
- **Ported subs (poorly designed):** Group delay 25ms+, extended ringing visible for 100ms+
- **Tapped horns:** Very fast decay above cutoff frequency, low group delay

### Perception Threshold

Not all group delay is audible. Studies suggest thresholds around 15–20ms for perception of group delay as "smearing" in bass frequencies, though this varies by frequency range and signal type. A well-designed ported sub at 15ms group delay may be perceptually equivalent to a sealed sub at 5ms for most program material.

## Relevance to Sonorant

"Fast transients" is a co-equal design constraint. This entry establishes the enclosure-level tradeoffs:

1. **Sealed alignment** offers the best intrinsic transient response but requires larger boxes or sacrificed extension to achieve Sonorant's infrasonic goals. A sealed sub flat to 25 Hz in a reasonable size requires a very long-throw driver with significant amplifier power.

2. **Ported alignment** can achieve the infrasonic extension Sonorant requires with manageable box size and power, but transient response suffers. Careful alignment (low port tuning, appropriate box Q) can minimize this, but some tradeoff is inherent.

3. **Horn loading** offers both transient response AND efficiency above its cutoff frequency, but achieving 20–30 Hz cutoff requires very large horns. Tapped horns (see separate entry) partially address this through their unique loading mechanism.

4. **Hybrid approaches** may be optimal: horn or tapped horn for 30–100 Hz (fast transients, high efficiency) with sealed or ported extension below 30 Hz (where transient concerns are less critical due to perceptual limits).

## Open Questions

- At what frequency does the audibility of group delay differences become negligible? (Below 30 Hz? 20 Hz?)
- Can active DSP correction (group delay equalization) make a ported sub behave like sealed for transients?
- What Qtc/alignment targets should Sonorant specify for acceptable transient performance?
