# Infrasonic Perception (Sub-20Hz Tactile Response)

**Status:** draft
**Confidence:** high
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Sources

1. Møller, H. & Pedersen, C.S. (2004). "Hearing at low and infrasonic frequencies." *Noise and Health*, 6(23), 37-57. [peer-reviewed]
2. ISO 226:2003. "Acoustics — Normal equal-loudness-level contours." International Organization for Standardization. [textbook/standard]
3. Watanabe, T. & Møller, H. (1990). "Low frequency hearing thresholds in pressure field and in free field." *Journal of Low Frequency Noise and Vibration*, 9(3), 106-115. [peer-reviewed]
4. Todd, N.P.M. & Cody, F.W. (2000). "Vestibular responses to loud dance music: A physiological basis for the 'rock and roll threshold'?" *Journal of the Acoustical Society of America*, 107(1), 496-500. [peer-reviewed]
5. Leventhall, G. (2007). "What is infrasound?" *Progress in Biophysics and Molecular Biology*, 93(1-3), 130-137. [peer-reviewed]

## Summary

Sound below 20 Hz is termed infrasound. Contrary to popular belief, infrasound is not inaudible — humans can perceive it if the sound pressure level is sufficiently high. At infrasonic frequencies, perception shifts from primarily auditory to primarily tactile/vibrational, with the chest cavity, abdomen, and vestibular system playing significant roles.

## Detail

### Hearing Thresholds at Low Frequencies

Hearing sensitivity decreases dramatically as frequency drops below 20 Hz, but auditory perception does not cease. Møller & Pedersen's comprehensive 2004 review established that humans can perceive infrasound at sufficiently high levels [1]:

- At **16 Hz**: threshold approximately 90–95 dB SPL
- At **8 Hz**: threshold approximately 100–105 dB SPL
- At **4 Hz**: threshold approximately 115–120 dB SPL

The ISO 226:2003 equal-loudness contours extend down to 20 Hz and show the steep rise in threshold below 100 Hz [2]. Below the standard's range, Møller and Watanabe's earlier work provides threshold data [3].

### Tactile vs. Auditory Perception

At frequencies below approximately 20 Hz, the sensation transitions from "hearing" to "feeling." This involves multiple mechanisms:

**Chest cavity resonance:** The thorax has resonant frequencies in the 50–100 Hz range, with some sensitivity extending lower. At high SPL, the chest wall and internal organs respond to pressure variations, creating distinct tactile sensations [5].

**Abdominal/visceral response:** The abdominal cavity and organs respond to infrasonic pressure, contributing to the "gut feeling" of powerful bass.

**Vestibular stimulation:** Todd & Cody found that very loud low-frequency sound can stimulate the vestibular system (inner ear balance organs), creating sensations of motion or disorientation. They proposed a "rock and roll threshold" around 90 dB at low frequencies where vestibular effects begin [4].

### SPL Requirements for Tactile Perception

Tactile perception of bass occurs at levels somewhat above the hearing threshold:

- **30–60 Hz range:** Strongest tactile response in the torso
- **50–100 Hz range:** Chest resonance effects most pronounced
- **Sub-30 Hz:** Requires very high SPL (100+ dB) for clear tactile sensation

At levels above the hearing threshold, Møller & Pedersen note that "it is possible to feel vibrations in various parts of the body" [1]. The sensation is distinct from auditory perception — subjects describe pressure, vibration, or movement rather than "sound."

### Perception Characteristics

Infrasonic perception has unique qualities:

- **No pitch sensation:** Below approximately 20 Hz, the sense of musical pitch disappears; perception becomes rhythmic/pulsing rather than tonal
- **Difficult to localize:** Very low frequencies are essentially omnidirectional in perception
- **Amplitude modulation sensitivity:** Fluctuations in infrasonic level (beating, modulation) are more perceptible than steady-state infrasound
- **Integration with higher frequencies:** Infrasonic content is often perceived as "weight" or "power" in conjunction with audible bass

## Relevance to Sonorant

"Sub weight" and "chest pressure, not just rumble" are explicit Sonorant goals. This entry establishes the physiological basis:

1. **Target frequencies:** True infrasonic "chest pressure" requires response below 30 Hz and ideally below 20 Hz. The 50–100 Hz chest resonance range is also critical for "felt" bass.

2. **SPL requirements:** Achieving tactile sensation requires high output capability. At 20 Hz, levels above 100 dB SPL may be needed for clear tactile perception. This has implications for driver excursion, enclosure size, and amplifier headroom.

3. **Perception mode:** Below 20 Hz, the sensation is not "bass you hear" but "pressure you feel." System design should optimize for clean, high-output sub-20Hz capability even though traditional frequency response measurements often ignore this range.

4. **Vestibular effects:** At sufficient levels, very low frequencies can create physical sensations beyond simple vibration. This may contribute to the "transported to another dimension" experiential goal.

## Open Questions

- What is the minimum sub-20Hz SPL required for the "chest pressure" sensation in a 100–200 cap room?
- How does room gain at low frequencies affect tactile perception thresholds?
- Is there a practical lower limit (e.g., 10 Hz, 5 Hz) below which the mechanical challenges outweigh perceptual benefit?
