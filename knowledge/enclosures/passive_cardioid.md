# Passive Cardioid Enclosure Techniques

**Status:** draft
**Confidence:** high
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Sources

1. Gunness, D.W. (2018). U.S. Patent No. 10,123,111 B2. "Passive cardioid speaker." Fulcrum Acoustic LLC. https://patents.google.com/patent/US10123111B2/en [patent]
2. Kang, J.Y. & Mathan, B. (2015). U.S. Patent No. 8,942,394 B2. "Cardioid loudspeaker array and method of operation." QSC Audio Products. [patent]
3. audioXpress. (2019). "Patent Review: Passive Cardioid Speaker." https://audioxpress.com/article/patent-review-passive-cardioid-speaker [industry]
4. Fulcrum Acoustic. "Passive Cardioid Technology." https://www.fulcrum-acoustic.com/audio-technology-insights-resources/passive-cardioid-technology/ [manufacturer]
5. ProSoundWeb. (2018). "Fulcrum Acoustic Awarded Patent For Passive Cardioid Loudspeaker." https://www.prosoundweb.com/fulcrum-acoustic-awarded-patent-for-passive-cardioid-loudspeaker/ [industry]

## Summary

Passive cardioid techniques achieve directional low-frequency radiation through enclosure geometry and acoustic filtering rather than active DSP or multiple-cabinet arrays. The Fulcrum Acoustic patent (US10,123,111 B2) represents the most developed implementation, using a higher-order acoustical low-pass filter to delay rear radiation and create frequency-dependent cardioid behavior from a single enclosure with a single amplifier channel.

## Detail

### The Problem: Omnidirectional Bass

At low frequencies, sound wavelengths are long relative to enclosure dimensions. A typical subwoofer cabinet is essentially omnidirectional below a few hundred Hz — it radiates equal energy in all directions. In many applications, this creates problems:

- **Rear wall coupling:** Energy directed backward excites room modes and reflects back with delay
- **Stage/performer interference:** In live sound, bass washing across the stage creates monitoring problems
- **Neighbor complaints:** In installations, rear radiation penetrates walls

Traditional solutions require multiple cabinets (end-fire arrays, gradient configurations) with DSP processing to create directional patterns. These are expensive, complex, and space-consuming.

### Passive Cardioid Principle

A cardioid radiation pattern (heart-shaped, with a null to the rear) can be created by combining two sources with appropriate delay and polarity. In a passive cardioid design:

1. The front of the driver diaphragm radiates forward (positive polarity)
2. The rear of the diaphragm (negative polarity relative to front) is routed through an acoustic circuit that delays and filters it
3. The delayed rear radiation exits through rear-facing ports
4. At the design frequency, the delayed rear output arrives in-phase with the forward radiation (constructive interference forward) and out-of-phase to the rear (destructive interference rearward)

### Fulcrum Patent (US10,123,111 B2) — Technical Details

**Inventor:** David W. Gunness
**Filing date:** June 3, 2016
**Grant date:** November 6, 2018
**Assignee:** Fulcrum Acoustic LLC

The patent describes a passive cardioid speaker using "an acoustical low-pass filter of order greater than one" composed of:

- **Elongated ducts:** Provide both acoustical mass (inductance) and propagation delay
- **Enclosed air volumes:** Provide acoustical compliance (capacitance)
- **Resistive elements:** Calibrated resistance for proper filter response

Key innovation over prior art: Earlier passive cardioid attempts used simple first-order filters (a port). Gunness's design uses second-order or higher filters, providing "greater flexibility with regard to the size, maximum output, and effective frequency range" [1].

The acoustic circuit modifies sound from the diaphragm's rear side such that the rear radiation is delayed by an appropriately designed acoustical system. The result is a single-input speaker producing directional low-frequency output without active electronics [3].

### Practical Implementation

Fulcrum's production subwoofers (CS121, CS118, CSX212, etc.) achieve:

- **Rear rejection:** Up to 10 dB reduction in rear radiation compared to front [4]
- **Single-cabinet operation:** No DSP required, no multiple-box arrays
- **Frequency range:** Effective roughly 40–120 Hz depending on model

### Comparison to Active Cardioid

| Aspect | Passive Cardioid | Active Cardioid Array |
|--------|------------------|----------------------|
| Cabinets required | 1 | 2+ |
| Amplifier channels | 1 | 2+ |
| DSP required | No | Yes |
| Setup complexity | Low | High |
| Flexibility | Fixed pattern | Adjustable |
| Bandwidth | Limited by acoustics | Broader |
| Rear rejection | ~10 dB | 15–20 dB possible |

### Limitations

- **Bandwidth:** Passive acoustic circuits are inherently narrowband — the cardioid behavior is strongest at specific frequencies and degrades above/below
- **Tuning sensitivity:** The acoustic circuit must be precisely tuned; manufacturing tolerances matter
- **Size constraints:** The delay path requires physical length, affecting cabinet dimensions
- **Fixed pattern:** Unlike active systems, the directionality cannot be adjusted for different venues

## Relevance to Sonorant

Passive cardioid is the most directly applicable innovation for Sonorant's small-room sub design:

1. **Single-cabinet simplicity:** Achieving rear rejection without arrays or DSP aligns with the modular, transportable goals. One sub per side with inherent directionality is simpler than managing end-fire arrays.

2. **Small-room benefit:** In 100–200 cap venues, the sub is often close to rear walls. Reducing rear radiation by 10 dB significantly decreases boundary-induced modal excitation and reflected bass that smears transients.

3. **Build feasibility:** The Fulcrum patent provides a documented approach. Understanding the acoustic circuit design could inform DIY implementations, though the patent is active.

4. **Tradeoff consideration:** Passive cardioid sacrifices some bandwidth flexibility for simplicity. Active cardioid systems offer more control but require more infrastructure. For a portable system, the passive approach may be optimal.

## Open Questions

- Can passive cardioid principles be applied to DIY designs without infringing the Fulcrum patent?
- What is the practical low-frequency limit for passive cardioid behavior (20 Hz? 30 Hz?)?
- How does passive cardioid performance compare in measured data to active end-fire arrays?
