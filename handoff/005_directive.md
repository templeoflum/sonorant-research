# Directive 005 — Vision Extraction, Knowledge Base Scaffolding & Research Queue

**From:** Planning instance (claude.ai)  
**To:** Transducer Archive (CLI agent)  
**Date:** 2025-02-05

## Objective

Extract the Sonorant Sound vision from raw conversation material, scaffold a knowledge base for future verified research, and build a research queue from topics identified in conversation logs. **No new research. No web lookups. No speculative content enters the repo.**

This directive treats the conversation logs (`reference_raw/conversation_logs.md`) as **source material to mine**, not as verified content. Three layers of extraction:

1. **Vision statements** — what the project is trying to achieve (extract and distill)
2. **Research questions** — topics worth investigating (extract as queue items, not answers)
3. **Speculative design output** — unverified brainstorming (leave in `reference_raw/`, do not import)

---

## PART A: Vision Extraction → VISION.md

### A1. Extract Core Vision

Read `reference_raw/conversation_logs.md` and extract all statements that define **what Sonorant Sound is trying to be** — the experiential goals, the design philosophy, the identity. These are statements of *intent*, not technical claims.

Distill into a structured `VISION.md` with these sections:

**1. Experiential Intent**
What the system is meant to make people *feel*. Draw from statements like:
- "utterly transcendent... transported to a completely different realm"
- "hyper real translation... sensual almost seductive intimacy"
- "communal and performative"
- "ripped violently out of this dimension... or transported gracefully into aural love making"
- "shows you what you need and didn't know you want... pushing you out of your comfort zone"

Distill these into a tight paragraph — no ChatGPT flourish, no "sonic entity" language. State the intent plainly and precisely.

**2. Sonic Priorities (Ranked)**
Extract and rank the core sonic goals from the conversation material. Based on what's documented:
1. Psychoacoustic immersion — spatial depth, envelopment, the "audio moment"
2. Sub weight — tactile, chest-presence bass with infrasonic extension (sub-30Hz, feel not just hear)
3. Hyper-real clarity — crystal clear vocals, high resolution for intricate soundscapes
4. Fast transients — snap, articulation, dynamic punch
5. Small-room optimization — 100–200 cap, reflection control, stage bleed management

Note: This ranking is derived from the emphasis pattern in conversation logs, not from a formal prioritization exercise. Flag this as needing user confirmation.

**3. Operational Parameters**
Extract the hard constraints stated in conversations:
- Venue scale: 100–200 capacity
- Use cases: small room, outdoors, portable
- Not fixed installation — transportable
- Open to stackable or low-profile form factor
- Signal chain: tunable, vinyl, DJ gear, live instruments
- Surround: late-stage goal, not immediate
- Listening system, not production monitoring
- Clarity over loudness

**4. Aesthetic Identity**
Extract what's been stated about the system's visual/cultural identity:
- "Glitchy mythopoetic cyber surrealism"
- No symbolic identity yet (name, sigil undecided)
- System as awakening tool — "viscerally more-real-than-real sonic activation"
- Range from gentle to violent

**5. Musical Context**
- Reference playlist: `https://open.spotify.com/playlist/0ss89af8ddF56e0xblrXIQ`
- Genre range: hyperpop → UKG → jungle → old-school dubstep → electronic (wide-genre electronic sets)
- Prioritize psychoacoustic enhancement over reference-style flat playback

### A2. Formatting Rules for VISION.md

- No marketing language. No "sonic entity" or "transcension engine" or "psychospiritual recalibration."
- Write plainly: what the system does, what it's for, what matters.
- Use the user's own words (quoted) where they're more precise than a summary.
- Flag anything that's ambiguous or contradictory as `[NEEDS CONFIRMATION]`.
- Include a `Last Updated` date and a note that this is v1.0 extracted from conversation logs.

---

## PART B: Knowledge Base Scaffolding

### B1. Create Directory Structure

Create the following empty directory structure under the repo root. Each directory gets a `_README.md` explaining what goes there and what standard the content must meet.

```
knowledge/
├── acoustics/
│   └── _README.md
├── transducers/
│   └── _README.md
├── psychoacoustics/
│   └── _README.md
├── enclosures/
│   └── _README.md
├── signal_processing/
│   └── _README.md
├── materials/
│   └── _README.md
├── references/
│   └── _README.md
└── _research_queue.md
```

### B2. Write Directory _README.md Files

Each `_README.md` should contain:
1. **Scope** — what topics belong in this directory (2–3 sentences)
2. **Content standard** — what a completed entry must include (source citation, confidence level, provenance)
3. **Entry format** — template for a knowledge entry (see B3)
4. **What does NOT belong** — speculative claims, unsourced assertions, manufacturer marketing

### B3. Knowledge Entry Template

Define a standard template that future directives will use to populate the knowledge base. Include this template in each `_README.md`:

```markdown
# [Topic Title]

**Status:** draft | reviewed | verified
**Confidence:** high | medium | low
**Sources:** [numbered list of sources with URLs or citations]
**Last Updated:** [date]
**Author:** [agent identifier]

## Summary
[2–3 sentence plain-language summary]

## Detail
[Full explanation with inline source citations, e.g. [1], [2]]

## Relevance to Sonorant
[How this topic connects to the project's experiential goals]

## Open Questions
[What remains unresolved or unverified]
```

### B4. Directory Scope Definitions

Use these scopes for each directory's `_README.md`:

**acoustics/** — Room acoustics, sound field behavior, radiation patterns, diffraction, reflection, absorption, standing waves, modal behavior. Focus on small-room (100–200 cap) behavior.

**transducers/** — Driver physics: motor theory (BL, inductance, eddy currents), cone behavior (breakup modes, materials), suspension mechanics, compression drivers, diaphragm materials. Thiele-Small parameters and their real-world implications.

**psychoacoustics/** — Human auditory perception: spatial hearing, HRTF, interaural differences, loudness perception, masking, precedence effect, envelopment vs. localization, the psychophysics of "immersion." Direct relevance to Sonorant's experiential goals.

**enclosures/** — Cabinet loading types and alignment theory: sealed, ported, bandpass, transmission line, tapped horn, Paraflex, horn-loaded, open baffle, hybrid designs. Port behavior, group delay, efficiency tradeoffs. Cardioid enclosure techniques (passive and active).

**signal_processing/** — Crossover theory (passive and active), FIR/IIR filter design, time alignment, phase correction, Temporal Equalization concepts, cardioid processing, DSP architectures. Not product-specific — principles and theory.

**materials/** — Cabinet materials (birch, composite, aluminum), cone/diaphragm materials (paper, polypropylene, aluminum, beryllium, carbon fiber), magnet materials (ferrite, neodymium, alnico), surround/spider materials. Properties that matter: density, damping factor, stiffness, thermal behavior.

**references/** — Verified book, paper, and lecture index. Each entry: title, author(s), year, format (book/paper/lecture/video), URL or DOI if available, brief relevance note. This is a bibliography, not a content repository.

---

## PART C: Research Queue Extraction → _research_queue.md

### C1. Extract Research Topics

Read through `reference_raw/conversation_logs.md` and extract every **topic** that was discussed, referenced, or suggested for study. Do NOT extract the answers or explanations — only the questions and topic areas.

For each topic, create an entry with:

```markdown
### [Topic Name]

**Category:** acoustics | transducers | psychoacoustics | enclosures | signal_processing | materials | references
**Priority:** high | medium | low
**Why it matters:** [1–2 sentences connecting to Sonorant's goals]
**Source in logs:** [brief description of where this appeared, e.g., "discussed in context of Fulcrum's passive cardioid patent"]
**Status:** queued
```

### C2. Expected Topics (Non-Exhaustive)

The conversation logs contain references to at least the following topics. Extract all of these plus any others you find:

**Transducers:**
- Thiele-Small parameters and enclosure alignment theory
- Voice coil inductance and eddy current losses (Leach 2002)
- BL(x), Cms(x), Le(x,i) nonlinearities (Klippel framework)
- Compression driver physics and horn loading
- Cone breakup modes and diaphragm resonance
- Neodymium magnet microstructure and thermal behavior
- Dual voice coil designs (e.g., KV2's Trans-Coil claims)

**Enclosures:**
- Tapped horn theory and alignment
- Paraflex / ROAR hybrid quarter-wave designs
- Passive cardioid enclosure techniques (Fulcrum patent US10,123,111 B2)
- Horn flare profiles: exponential, tractrix, Le Cléac'h, oblate spheroidal
- Port turbulence, thermoviscous losses, and chuffing
- Open baffle / dipole / Ripole designs
- PPSL (push-pull slot-loaded) and isobaric configurations

**Acoustics:**
- Small-room modal behavior and treatment
- Boundary coupling effects at low frequencies
- Near-field vs. far-field behavior in small venues
- Diffraction and baffle effects on imaging

**Psychoacoustics:**
- Spatial hearing: HRTF, interaural time/level differences
- Precedence effect and Haas effect in small rooms
- Envelopment vs. localization — what creates "immersion"
- Infrasonic perception (sub-20Hz tactile response)
- Loudness perception curves and equal-loudness contours

**Signal Processing:**
- FIR vs. IIR crossover design tradeoffs
- Temporal Equalization (TQ) concepts (Fulcrum/Gunness)
- Active cardioid processing for LF directivity
- Phase alignment techniques for multi-way systems
- All-pass networks and group delay management

**Materials:**
- Viscoelasticity in cone and suspension materials
- Constrained-layer damping for cabinets
- Composite enclosure construction (fibreglass, carbon)
- Thermal management: copper shorting rings, ferrofluid, heat pipes

**References (to catalog, not study):**
- Beranek & Mellow — Acoustics: Sound Fields and Transducers
- Borwick — Loudspeaker & Headphone Handbook
- Leach — Introduction to Electroacoustics & Audio Amplifier Design
- Thiele + Small original papers
- Klippel tutorials/papers on loudspeaker nonlinearities
- Floyd Toole — Sound Reproduction
- Linkwitz Lab essays on baffle/diffraction/dispersion
- Earl Geddes — waveguide/horn design work
- NPTEL IIT Kharagpur electro-acoustics lectures

### C3. Formatting Rules for _research_queue.md

- Header with explanation: "Topics extracted from conversation logs for future verified research. None of the explanations or claims from those logs are imported — only the questions."
- Group by category (matching the knowledge/ directory structure)
- Sort within category by priority (high → medium → low)
- Priority assignment logic:
  - **High** = directly relevant to Sonorant's stated goals (small-room, psychoacoustic, sub-bass, clarity)
  - **Medium** = relevant to speaker design generally, useful context
  - **Low** = interesting but tangential, future consideration
- Include a count at the top: "X topics queued across Y categories"

---

## PART D: Update DEVLOG.md

Add Entry 7:

**Entry 7 — Vision Extraction & Knowledge Base Scaffolding (Directive 005)**
- Extracted Sonorant Sound vision from conversation logs into VISION.md
- Created knowledge base directory structure with entry templates and standards
- Built research queue from conversation logs — extracted topics, not answers
- Established three-layer triage for conversation log material: vision (import), research questions (queue), speculative design (leave in reference_raw/)
- [Include count of topics extracted and any notable patterns in what was found]
- Open question: research queue priorities need user review and confirmation

---

## PART E: Update README.md

Add to the "File Structure" section:
- `VISION.md` — Sonorant Sound experiential goals and design parameters (extracted from conversation logs)
- `knowledge/` — Verified research entries organized by topic (currently empty, populated by future directives)
- `knowledge/_research_queue.md` — Topics queued for investigation

Update "What's Next" to replace the three candidate paths with:
1. **Populate knowledge base** — begin verified research on high-priority queue topics (start with psychoacoustics and enclosures, highest relevance to Sonorant goals)
2. **Batch 2 company research** — additional boutique manufacturers or major manufacturer baselines
3. **Design synthesis** — cross-reference company report findings with knowledge base entries to identify candidate topologies

Note that path 1 is recommended before path 3, since design synthesis requires a verified knowledge base to draw from.

---

## Scope Boundaries

- **DO:** Read conversation logs and extract vision, topics, and references
- **DO:** Create all directory structures and template files
- **DO:** Write VISION.md, _research_queue.md, and all _README.md files
- **DO:** Update DEVLOG.md and README.md
- **DO NOT:** Conduct any web research or verify any claims from the logs
- **DO NOT:** Import explanations, speculative designs, or technical claims from the logs into the repo
- **DO NOT:** Create knowledge entries (the directories should contain only _README.md files)
- **DO NOT:** Edit any existing report files (JSON or markdown)
- **DO NOT:** Edit historical handoff files (001–004 responses/directives)
- **DO NOT:** Run git commands — the user handles repo operations

---

## Deliverables

1. **VISION.md** — Sonorant Sound vision document (root of repo)
2. **knowledge/** directory tree with `_README.md` in each subdirectory
3. **knowledge/_research_queue.md** — complete research topic queue
4. **Updated README.md** — with new file structure and next steps
5. **Updated DEVLOG.md** — with Entry 7
6. **005_response.md** containing:
   - Summary of vision extraction (key themes, any contradictions found)
   - Research queue statistics (topics per category, priority distribution)
   - List of all files created/modified
   - Any ambiguities or items flagged for user confirmation

---

## Verification Checklist (Self-Check Before Submitting)

- [ ] VISION.md contains no marketing language or ChatGPT flourish
- [ ] VISION.md uses user's own words (quoted) where more precise than summary
- [ ] VISION.md flags ambiguities as `[NEEDS CONFIRMATION]`
- [ ] All knowledge/ subdirectories exist with _README.md files
- [ ] Each _README.md has scope, content standard, entry template, exclusion criteria
- [ ] _research_queue.md extracts topics only — no explanations or claims imported
- [ ] _research_queue.md is grouped by category and sorted by priority
- [ ] _research_queue.md includes topic count in header
- [ ] No speculative design content from logs entered the repo
- [ ] No web research was conducted
- [ ] No existing report files were modified
- [ ] DEVLOG.md has Entry 7
- [ ] README.md updated with knowledge base structure and revised next steps
- [ ] No historical handoff files were edited
