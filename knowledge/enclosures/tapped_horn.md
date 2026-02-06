# Tapped Horn Theory and Alignment

**Status:** draft
**Confidence:** high
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Sources

1. Danley, T.J. (2007). U.S. Patent No. 8,457,341 B2. "Sound reproduction with improved low frequency characteristics." https://patents.google.com/patent/US8457341B2/en [patent]
2. Ricci, J. "Skhorn Subwoofer & Files." Data-Bass Forums. https://data-bass.ipbhost.com/topic/613-riccis-skhorn-subwoofer-files/ [community]
3. Cowan Audio. "Tapped Horn Experiments." https://www.cowanaudio.com/th.html [community]
4. diyAudio. "Evolution of the Tapped Horn." https://www.diyaudio.com/community/threads/evolution-of-the-tapped-horn.135879/ [community]
5. audioXpress. "Patent Review: Compact Wideband Bass and Midrange Horn-Loaded Speaker System." https://audioxpress.com/article/patent-review-compact-wideband-bass-and-midrange-horn-loaded-speaker-system [industry]

## Summary

A tapped horn places the driver partway along a folded horn path, coupling the front and rear of the driver diaphragm to different points in the horn. This allows the rear wave to reinforce the front wave at specific frequencies, extending bandwidth and improving efficiency compared to front-loaded horns of similar size. Tapped horns are a primary candidate for achieving Sonorant's infrasonic extension goals in a manageable format.

## Detail

### Operating Principle

In a conventional front-loaded horn, the driver sits at the throat; the rear of the driver fires into a sealed or vented chamber. In a tapped horn:

1. The driver is mounted at an intermediate position in the horn path
2. The front of the driver couples to one section of the horn (the downstream/mouth section)
3. The rear of the driver couples through an internal path to another section (the upstream/throat section)
4. Both outputs eventually emerge from the horn mouth

The key is that the rear wave travels a longer path than the front wave. At the frequency where the path difference equals half a wavelength, the two waves arrive in phase at the mouth, reinforcing each other [1].

### Tom Danley's Patent (US 8,457,341 B2)

**Filed:** 2007 | **Granted:** 2013

Danley's patent describes "a compact high-fidelity sound reproduction system achieving high efficiency, low distortion, wide bandwidth, and extended low-frequency reach" [1].

Key design elements:

- **Driver position:** At the throat of the downstream section, with rearward output communicating with the upstream section
- **Tap point:** Where output from both paths merges, located at the beginning of the downstream section
- **Path length:** Total approximately one-quarter wavelength at the design frequency
- **Tap position:** Driver placed at roughly 1/4 to 1/3 of the way from the mouth [3]

The upstream path (behind the driver) has little or no expansion, functioning more like a duct than a horn. The downstream path (in front of the driver) expands toward the mouth.

### Bandwidth Extension Mechanism

The tapped configuration creates beneficial summation at multiple frequencies:

1. **Quarter-wave frequency:** The total horn length produces reinforcement at f where λ = 4L
2. **Half-wave frequency of tap path:** The rear-wave path length produces additional reinforcement
3. **Horn mouth loading:** Above cutoff, normal horn loading provides efficiency

This multi-mechanism loading extends usable bandwidth compared to:
- Ported boxes (limited by port tuning)
- Simple front-loaded horns (limited by horn cutoff)

### Josh Ricci's Designs (SKHORN, SKRAM, MAUL)

Ricci developed several tapped horn / 6th-order bandpass designs with extensive Data-Bass measurements [2]:

**SKHORN:**
- Quasi 6th-order bandpass with horn-loaded upper end
- Opposed driver arrangement (reduces vibration)
- 15–21" driver options
- Measured usable response to ~25–30 Hz depending on driver

**SKRAM:**
- More compact 6th-order bandpass design
- Optimized for high-efficiency drivers
- Usable output to approximately 30 Hz
- "Fairly reasonable box size" for output capability

**Key measured characteristics:**
- Very low ringing/group delay above cutoff frequency
- Clean waterfall plots showing fast energy decay
- High efficiency (low amplifier power required)

### Comparison to Other Sub Topologies

| Topology | Deep extension | Efficiency | Size | Transients |
|----------|---------------|------------|------|------------|
| Sealed | Moderate | Low | Small | Excellent |
| Ported | Good | Medium | Medium | Good |
| Tapped horn | Good | High | Large | Excellent |
| Front-loaded horn | Limited by cutoff | Very high | Very large | Excellent |
| Bandpass (4th/6th) | Good | High | Medium-Large | Variable |

Tapped horns occupy a middle ground: better efficiency than ported, better extension than front-loaded horns of similar size, excellent transient response above cutoff.

### Design Challenges

- **Size:** Achieving 20–30 Hz extension requires substantial path length (8–12+ feet folded)
- **Complexity:** The folded path requires careful internal bracing and precise dimensions
- **Driver matching:** Not all drivers work well; requires appropriate Thiele-Small parameters
- **Single-frequency optimization:** Peak efficiency occurs at the design frequency; response shape is fixed

## Relevance to Sonorant

Tapped horns are a primary candidate for Sonorant's sub architecture:

1. **Infrasonic extension:** Well-designed tapped horns reach 25–30 Hz with authority — approaching the "sub-30Hz felt in the body" goal.

2. **Efficiency:** High sensitivity means less amplifier power required, improving transportability and reducing heat/weight.

3. **Transient response:** Above cutoff frequency, tapped horns provide excellent damping and fast decay — serving the "fast transients" constraint.

4. **Community documentation:** Ricci's SKHORN/SKRAM designs are well-documented with public plans and measurements, providing a potential DIY path.

5. **Size tradeoff:** The main challenge is physical size. A 20 Hz tapped horn is large. For 100–200 cap venues, this may be acceptable; for extreme portability, it may not be.

6. **Hybrid potential:** Tapped horn for 30–80 Hz combined with sealed/ported extension for 20–30 Hz could optimize across all constraints.

## Open Questions

- What is the practical lower limit for tapped horn extension in a transportable format?
- Can smaller tapped horn designs (optimized for 40 Hz+) be combined with separate infrasonic extension?
- How do Ricci's designs compare to Danley's commercial TH series in measured performance?
- What driver parameters are optimal for tapped horn loading in the 20–40 Hz range?
