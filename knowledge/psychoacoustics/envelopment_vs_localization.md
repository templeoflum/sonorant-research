# Envelopment vs. Localization — What Creates "Immersion"

**Status:** draft
**Confidence:** high
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Sources

1. Barron, M. & Marshall, A.H. (1981). "Spatial impression due to early lateral reflections in concert halls: The derivation of a physical measure." *Journal of Sound and Vibration*, 77(2), 211-232. [peer-reviewed]
2. Bradley, J.S. & Soulodre, G.A. (1995). "Objective measures of listener envelopment." *Journal of the Acoustical Society of America*, 98(5), 2590-2597. [peer-reviewed]
3. Griesinger, D. "General overview of spatial impression, envelopment, localization." http://davidgriesinger.com/overvw1.pdf [industry]
4. Morimoto, M. & Maekawa, Z. (1988). "Effects of low frequency components on auditory spaciousness." *Acustica*, 66, 190-196. [peer-reviewed]
5. Hidaka, T., Beranek, L.L., & Okano, T. (1995). "Interaural cross-correlation, lateral fraction, and low- and high-frequency sound levels as measures of acoustical quality in concert halls." *Journal of the Acoustical Society of America*, 98(2), 988-1007. [peer-reviewed]

## Summary

Spatial impression in reproduced sound consists of two distinct perceptual dimensions: Apparent Source Width (ASW), which relates to the perceived size of the sound source, and Listener Envelopment (LEV), which relates to the sensation of being surrounded by sound. These are created by different physical mechanisms and measured by different acoustic parameters.

## Detail

### Definitions

**Apparent Source Width (ASW)** is defined as the width of a sound image fused temporally and spatially with the direct sound [4]. It describes how "large" a source appears — a wide ASW makes instruments or voices seem to occupy more space than their physical size.

**Listener Envelopment (LEV)** is defined as the degree of fullness of sound images around the listener, excluding the sound image composing ASW [4]. It describes the sensation of being immersed or surrounded by reverberant sound.

### Physical Measures

**Early Lateral Energy Fraction (LFE)** — the ratio of early lateral sound energy (arriving within 80ms, from the sides) to total early sound energy — correlates strongly with ASW [1]. Higher LFE produces wider apparent sources.

**Late Lateral Sound Level (LJ)** — the level of late lateral reflections (after 80ms) — correlates strongly with LEV [2]. Bradley and Soulodre found that LJ best predicts listener envelopment ratings.

**Interaural Cross-Correlation Coefficient (IACC)** — measures the similarity between signals at the two ears. Low IACC (dissimilar ear signals) correlates with high spaciousness [5]. IACC can be computed separately for early reflections (IACCE, related to ASW) and late reflections (IACCL, related to LEV).

### The Role of Lateral Reflections

The foundational work of Marshall, Barron, and Barron & Marshall established that early lateral reflections (arriving from the sides within approximately 80ms of the direct sound) are the primary physical cause of spatial impression [1]. Sound arriving from directly ahead or behind produces high interaural correlation and minimal spatial effect; sound arriving from the sides produces low correlation and strong spaciousness.

For LEV specifically, Morimoto and Maekawa showed that the degree of interaural cross-correlation of late reflections relates to envelopment [4]. Late reflections arriving from multiple directions create the sense of being "inside" the sound field rather than observing it from outside.

### Envelopment vs. Localization

These are complementary, not competing, phenomena:

- **Localization** depends on the precedence effect and direct sound — the brain uses the first-arriving wavefront to determine source position
- **Envelopment** depends on diffuse late reflections — the brain interprets decorrelated signals at the ears as evidence of being surrounded

A well-designed system can maintain precise localization (tight imaging of sources) while simultaneously providing strong envelopment (the sense of being immersed in the acoustic space). The key is temporal separation: early sound (0–80ms) carries localization cues; late sound (>80ms) carries envelopment cues.

## Relevance to Sonorant

"Psychoacoustic immersion" is a co-equal design constraint for Sonorant Sound. This entry establishes what that means in measurable terms:

1. **For envelopment:** The system needs to generate or preserve lateral energy. In a small room, wall reflections provide this naturally, but speaker directivity affects how much energy reaches side walls. Wider dispersion may increase envelopment but can also increase interference. Room treatment choices trade envelopment against clarity.

2. **For source width:** Early reflections widen apparent sources. In nearfield/small-room contexts, the listener is often within the critical distance where direct sound dominates — this can reduce ASW. Deliberate use of early reflection management (or speaker design that controls early radiation pattern) can optimize this balance.

3. **The distinction matters:** A system optimized only for "spaciousness" might sacrifice localization precision. Sonorant requires both — precise imaging AND envelopment. This likely means controlled directivity in the direct sound path combined with managed reflections for ambience.

## Open Questions

- What specific LFE and LJ targets are appropriate for 100–200 cap rooms vs. concert halls (where most research was conducted)?
- How does nearfield listening (typical in small rooms) affect the ASW/LEV balance?
- Does bass contribute to envelopment, or is this primarily a mid/high frequency phenomenon?
