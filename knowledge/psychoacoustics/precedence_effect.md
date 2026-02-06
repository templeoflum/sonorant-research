# Precedence Effect and Haas Effect in Small Rooms

**Status:** draft
**Confidence:** high
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Sources

1. Litovsky, R.Y., Colburn, H.S., Yost, W.A., & Guzman, S.J. (1999). "The precedence effect." *Journal of the Acoustical Society of America*, 106(4), 1633-1654. [peer-reviewed]
2. Haas, H. (1972). "The influence of a single echo on the audibility of speech." *Journal of the Audio Engineering Society*, 20(2), 146-159. (English translation of 1951 German thesis) [peer-reviewed]
3. Blauert, J. (1997). *Spatial Hearing: The Psychophysics of Human Sound Localization*. MIT Press. [textbook]
4. Everest, F.A. & Pohlmann, K.C. (2015). *Master Handbook of Acoustics*, 6th Edition. McGraw-Hill. [textbook]
5. Olive, S.E. & Toole, F.E. (1989). "The detection of reflections in typical rooms." *Journal of the Audio Engineering Society*, 37(7/8), 539-553. [peer-reviewed]

## Summary

The precedence effect (also called the Haas effect or law of the first wavefront) describes how the auditory system integrates early reflections with the direct sound, allowing localization based on the first-arriving wavefront while suppressing echo perception of closely-following reflections. The integration window is approximately 5–40ms depending on signal complexity. In small rooms, understanding this effect is critical for speaker placement and acoustic treatment.

## Detail

### Core Mechanism

The precedence effect refers to a group of phenomena involved in resolving competition for perception and localization between a direct sound and its reflections [1]:

1. **Fusion:** When two similar sounds arrive within a short time window, they are perceived as a single auditory event rather than separate sounds
2. **Localization dominance:** The perceived location of the fused sound is determined primarily by the first-arriving wavefront
3. **Lag discrimination suppression:** The ability to detect changes in the lagging sound is reduced

### Integration Window

The time window for fusion depends on signal complexity [1][3]:

- **Simple transients (clicks):** ~5ms integration window
- **Complex sounds (speech, music):** up to 40ms integration window

Within this window, a reflection can be up to 10 dB louder than the direct sound without being perceived as a separate echo [2]. This is the Haas effect proper — Haas showed that for delays between 10–30ms, the delayed sound can be significantly louder without disrupting localization of the source.

### Breakdown Conditions

The precedence effect breaks down when:

- **Delay exceeds the integration window:** Reflections arriving after ~40ms (for complex sounds) begin to be heard as distinct echoes
- **Level difference is too extreme:** If the reflection is much louder than the direct sound, localization shifts toward the reflection
- **Spectral content differs:** If direct and reflected sounds have different frequency content, fusion may be incomplete
- **Repetition:** Repeated exposure to lead-lag pairs can "build up" and then "break down" the precedence effect [1]

### Small Room Implications

In rooms typical of 100–200 cap venues, wall reflections arrive quickly:

| Room dimension | Reflection delay (single bounce) |
|----------------|----------------------------------|
| 3m (10 ft) | ~9ms |
| 5m (16 ft) | ~15ms |
| 10m (33 ft) | ~29ms |

At these dimensions, most first reflections fall within the integration window and will fuse with the direct sound rather than being heard as echoes. This has several consequences:

**Positive effects:**
- Early lateral reflections contribute to spatial impression (ASW, LEV) without creating echo perception
- The room "supports" the sound rather than adding confusion

**Negative effects:**
- Reflections arriving 5–20ms after direct sound can cause comb filtering when they combine with the direct signal
- Multiple reflections arriving within the window can smear transients even if they don't create audible echoes
- Image stability may suffer if early reflections arrive from different directions than the direct sound

### Reflection Management Strategies

Olive & Toole's research on reflection detection in typical rooms [5] found that:

- Listeners are remarkably tolerant of reflections within the integration window
- Detection thresholds are higher for lateral reflections than for reflections from the same direction as the source
- Absorptive treatment at first reflection points reduces coloration but may reduce beneficial spatial impression

The optimal strategy depends on goals: maximum clarity favors absorption; maximum spaciousness favors reflection; Sonorant's co-equal constraints require balance.

## Relevance to Sonorant

In 100–200 cap rooms, listeners are close to boundaries. The precedence effect determines whether those boundaries help or hurt:

1. **Speaker placement:** Distance from walls affects reflection timing. Placing speakers very close to walls produces reflections within ~5ms, which fuse tightly but may cause tonal coloration. Placing speakers far from walls (if room permits) pushes first reflections later in the integration window.

2. **Treatment decisions:** Absorbing first reflection points improves image precision and transient clarity but reduces envelopment. Diffusing first reflection points maintains envelopment while reducing comb filtering. The choice affects all five sonic priorities differently.

3. **Transient response:** "Fast transients" is a co-equal constraint. Reflections within the integration window don't create audible echoes but do affect transient perception by smearing the attack. Directivity control (narrower coverage) reduces this effect by putting less energy into early reflections.

4. **Small-room optimization:** The 100–200 cap scale means short reflection paths. Almost all reflections will be within the integration window — this is fundamentally different from concert hall acoustics where many reflections exceed 40ms.

## Open Questions

- What is the optimal first-reflection delay for balancing clarity and spaciousness in Sonorant's target venues?
- How does the integration window interact with bass frequencies where wavelengths exceed room dimensions?
- Should directivity be frequency-dependent (narrow HF, wider LF) to optimize reflection management?
