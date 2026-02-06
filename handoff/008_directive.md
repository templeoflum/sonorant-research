# Directive 008 — Architecture-Agnostic Cleanup & First Knowledge Base Population

**From:** Planning instance (claude.ai)  
**To:** Transducer Archive (CLI agent)  
**Date:** 2025-02-05

## Context

Directive 007 completed the aesthetic identity overhaul and sonic priority restructure. During post-007 review, one residual issue was identified: AGENT_PLAN.md still contains MEH-centric language in its mission statement and research tracks that contradicts the architecture-agnostic stance established across directives 002–007. The system architecture is explicitly OPEN — no topology is pre-selected.

Separately, the knowledge base was scaffolded in Directive 005 (7 directories, entry templates, 47-topic research queue) but remains completely empty. No verified research entries exist yet. This directive begins populating it with a first batch of 7 high-priority topics selected for their foundational relevance — these are the topics that other research builds on.

Additionally, README.md's file structure tree is outdated — it's missing `knowledge/`, `VISION.md`, and `PLANNING_LOG.md`.

## Objective

Three-part directive:
1. Fix architecture-biased language in AGENT_PLAN.md
2. Update README.md file structure to reflect current repo
3. Populate 7 knowledge base entries from the research queue using verified sources

This directive **requires web research** for Part C.

---

## Part A: AGENT_PLAN.md — Remove MEH Bias

### A1: Mission Statement

In Part 3 (Research Agent Specification), find the mission statement:

> Compile verified, source-grounded technical intelligence on loudspeaker companies, designs, patents, and deployments — structured for cross-brand comparison and synthesis into Sonorant Sound's MEH-based system.

Replace with:

> Compile verified, source-grounded technical intelligence on loudspeaker companies, designs, patents, and deployments — structured for cross-brand comparison and synthesis into Sonorant Sound's system design. No topology is pre-selected; the research exists to surface all viable architectures.

### A2: Step 3 in "Next Steps" (Part 4)

Find:

> **Step 3: MEH-Specific Research Track**
> Dedicated deep dive on multi-entry horn lineage:

Replace the heading and intro with:

> **Step 3: Topology-Specific Research Tracks**
> Deep dives on candidate architectures identified through company research. MEH is one track among several:

Keep the existing MEH bullet list but add after it:

```markdown
**Other topology tracks (equal priority):**
- Passive cardioid sub techniques (Fulcrum patent US10,123,111 B2)
- Coaxial point-source designs (Fulcrum, KV2 approach)
- Tapped horn sub alignments (Ricci SKHORN/SKRAM, Danley)
- Horn-loaded fullrange approaches (Funktion-One philosophy)
- Active cardioid/gradient LF configurations
```

### A3: Global check

Search AGENT_PLAN.md for any remaining instances where MEH or Synergy Horn is framed as *the* target architecture rather than *a* candidate. If found, rewrite to architecture-neutral framing. Do not remove MEH references entirely — it remains a valid candidate — just ensure it's presented as one option among many.

---

## Part B: README.md — Update File Structure

### B1: File Structure Tree

The current file structure tree in README.md is outdated. Replace the entire tree with:

```
sonorant-research/
├── README.md                           # This file
├── VISION.md                           # Experiential goals, sonic priorities, aesthetic identity
├── PLANNING_LOG.md                     # Current project decisions with rationale (domain-organized)
├── DEVLOG.md                           # Chronological decision log
├── AGENT_PLAN.md                       # Research agent specification
├── STANDARDS.md                        # Uniform Data Standard reference
├── .gitignore
│
├── schema/
│   └── uds_v1.md                       # UDS v1.1 — scoring, schemas, tech vocabulary
│
├── knowledge/
│   ├── _research_queue.md              # 47-topic research queue across 7 domains
│   ├── acoustics/                      # Room acoustics, radiation, modal behavior
│   ├── enclosures/                     # Cabinet loading, alignment theory, horn design
│   ├── transducers/                    # Driver physics, motor theory, diaphragm behavior
│   ├── psychoacoustics/                # Human auditory perception, spatial hearing, immersion
│   ├── signal_processing/              # Crossovers, DSP, phase alignment, FIR/IIR
│   ├── materials/                      # Cone, cabinet, magnet materials and properties
│   └── references/                     # Verified bibliography of key texts and papers
│
├── reports/
│   └── boutique/
│       ├── danley_sound_labs.md/.json
│       ├── fulcrum_acoustic.md/.json
│       ├── funktion_one.md/.json
│       ├── hennessey_sound_design.md/.json
│       ├── holoplot.md/.json
│       ├── kv2_audio.md/.json
│       ├── pk_sound.md/.json
│       ├── void_acoustics.md/.json
│       └── _indexes/
│           ├── companies.csv
│           └── models.csv
│
└── handoff/
    ├── 001_directive.md / 001_response.md
    ├── ...
    └── 008_directive.md / 008_response.md
```

### B2: Status Table

Add to the status section:

```
| 008 | Architecture-agnostic cleanup + first knowledge base population | ✅ Complete |
```

---

## Part C: Knowledge Base Population — Batch 1 (7 Topics)

Research and write verified knowledge base entries for the following 7 topics. These were selected from `knowledge/_research_queue.md` as the most foundational — other topics in the queue build on these.

### Entry Format

Follow the template established in each directory's `_README.md`:

```markdown
# [Topic Title]

**Status:** draft
**Confidence:** [high | medium | low]
**Sources:** [numbered list with URLs, DOIs, or full citations]
**Last Updated:** 2025-02-05
**Author:** Transducer Archive (CLI agent)

## Summary
[2–3 sentence plain-language summary]

## Detail
[Full explanation with inline source citations, e.g. [1], [2]]

## Relevance to Sonorant
[How this connects to the project's experiential goals and design constraints]

## Open Questions
[What remains unresolved or unverified]
```

### Source Requirements

- Every factual claim must have a source citation (resolvable URL, DOI, or full bibliographic reference)
- Provenance: tag each source as `peer-reviewed`, `textbook`, `industry` (trade press, AES convention papers), `manufacturer`, or `community` (forums, DIY)
- Minimum 3 sources per entry; prefer peer-reviewed and textbook sources over manufacturer claims
- If sources conflict, document both values with provenance
- Unknown = state "not established" — never estimate or infer

### Topic 1: Envelopment vs. Localization — What Creates "Immersion"

**File:** `knowledge/psychoacoustics/envelopment_vs_localization.md`  
**Queue priority:** high

Research the psychoacoustic distinction between listener envelopment (LEV) and auditory source width (ASW). Cover: how lateral reflections create envelopment, the role of interaural cross-correlation (IACC), the difference between feeling "surrounded by sound" vs. "locating a source," and what loudspeaker system parameters contribute to each. Reference Griesinger, Barron, Bradley as primary sources.

**Relevance hook:** Sonorant's core goal is "psychoacoustic immersion" — this entry defines what that means in measurable terms.

### Topic 2: Infrasonic Perception (Sub-20Hz Tactile Response)

**File:** `knowledge/psychoacoustics/infrasonic_perception.md`  
**Queue priority:** high

Research how humans perceive sound below 20Hz. Cover: tactile vs. auditory perception thresholds, the role of chest cavity and visceral resonance, bone conduction at infrasonic frequencies, SPL levels required for tactile perception, and any documented psychophysiological effects. Reference Todd, Møller, and ISO 226.

**Relevance hook:** Sonorant targets "chest pressure, not just rumble" — this entry establishes what frequencies and levels produce that sensation.

### Topic 3: Precedence Effect and Haas Effect in Small Rooms

**File:** `knowledge/psychoacoustics/precedence_effect.md`  
**Queue priority:** high

Research the precedence effect (Haas effect): fusion of early reflections with direct sound, the integration window (~5–40ms), conditions for localization dominance, and how it breaks down. Cover implications for small-room loudspeaker deployment: reflection timing at 100–200 cap venue scales, how room dimensions affect the integration window, and speaker placement strategies.

**Relevance hook:** In 100–200 cap rooms, listeners are close to boundaries. Understanding when reflections help (envelopment) vs. hurt (comb filtering, image shift) is essential.

### Topic 4: Passive Cardioid Enclosure Techniques

**File:** `knowledge/enclosures/passive_cardioid.md`  
**Queue priority:** high

Research passive cardioid sub techniques — achieving directional LF radiation through enclosure geometry and acoustic resistance rather than active arrays. Primary source: Fulcrum Acoustic patent US10,123,111 B2 (Gunness & Hoy). Also cover: the general principle of rear-firing driver + delay path, historical precedents (Kang & Mathan), practical limitations (bandwidth, tuning sensitivity), and comparison to active cardioid approaches. Access and cite the actual patent text.

**Relevance hook:** Most directly applicable innovation for Sonorant's small-room sub design — rear rejection without needing multiple cabinets or DSP processing.

### Topic 5: Sealed vs. Ported vs. Horn — Transient Response Tradeoffs

**File:** `knowledge/enclosures/alignment_transient_tradeoffs.md`  
**Queue priority:** high

Research how the three major enclosure alignments differ in transient behavior. Cover: group delay characteristics of each, impulse response differences, how alignment affects "punch" and "tightness" perception, the relationship between enclosure Q and transient ringing, and measured examples where available. Reference Small/Thiele foundational papers, Dickason, and any AES papers comparing time-domain performance across alignments.

**Relevance hook:** "Fast transients" is a co-equal design constraint. This entry establishes which enclosure approaches best serve that goal and at what cost.

### Topic 6: Tapped Horn Theory and Alignment

**File:** `knowledge/enclosures/tapped_horn.md`  
**Queue priority:** high

Research tapped horn operating principles: the driver positioned partway along a horn, coupling to both throat and mouth simultaneously, bandwidth extension mechanism, efficiency characteristics. Cover: Danley patent lineage, the community-developed designs (Ricci SKHORN/SKRAM with data-bass.com measurements), alignment parameters, practical size/output tradeoffs, and comparison to other sub topologies for infrasonic extension.

**Relevance hook:** Tapped horns are a primary candidate for Sonorant's sub architecture — high efficiency and deep extension in a manageable format.

### Topic 7: Small-Room Modal Behavior and Treatment

**File:** `knowledge/acoustics/small_room_modes.md`  
**Queue priority:** high

Research room mode behavior in small venues (dimensions typical of 100–200 cap spaces). Cover: axial, tangential, and oblique modes, the Schroeder frequency and its implications, bass buildup at boundaries, null patterns, and practical treatment approaches (absorption, diffusion, trap placement). Include the math for calculating room modes from dimensions. Reference Everest, Toole, and any AES/ASA papers on small-room acoustics.

**Relevance hook:** Every Sonorant deployment will be in a different small room. Understanding modal behavior is prerequisite for system tuning and placement strategy.

### C2: Research Queue Updates

After completing the entries, update `knowledge/_research_queue.md`:
- Change status from `queued` to `populated` for all 7 topics
- Add a note at the top: "7 of 47 topics populated (Directive 008)"

---

## Part D: DEVLOG.md — Add Entry 10

Append:

```markdown
## Entry 10 — Architecture-Agnostic Cleanup & First Knowledge Base Population (Directive 008)

**Date:** 2025-02-05
**Phase:** Directive 008

### What Happened
- Fixed MEH-biased language in AGENT_PLAN.md mission statement and research tracks
- Updated README.md file structure to reflect current repo state
- Populated first 7 knowledge base entries from verified research

### Key Decisions and Rationale

**AGENT_PLAN.md cleanup:** Mission statement referenced "MEH-based system" — contradicts the architecture-agnostic stance established since Directive 002. Fixed to reflect open topology. MEH research track reframed as one track among several topology-specific deep dives.

**Knowledge base topic selection:** First batch chosen for foundational relevance — these 7 topics underpin decisions across all other research. Three from psychoacoustics (defining what "immersion" actually means), three from enclosures (the core sub and alignment decisions), one from acoustics (the room itself). Topics were selected so that future entries can reference these as established foundations.

### Files Changed
- AGENT_PLAN.md — Mission statement and Step 3 rewritten
- README.md — File structure tree updated, status table updated
- knowledge/psychoacoustics/envelopment_vs_localization.md — Created
- knowledge/psychoacoustics/infrasonic_perception.md — Created
- knowledge/psychoacoustics/precedence_effect.md — Created
- knowledge/enclosures/passive_cardioid.md — Created
- knowledge/enclosures/alignment_transient_tradeoffs.md — Created
- knowledge/enclosures/tapped_horn.md — Created
- knowledge/acoustics/small_room_modes.md — Created
- knowledge/_research_queue.md — Updated (7 topics marked populated)
- DEVLOG.md — This entry

### Surprises or Pattern Shifts
[Agent: note any unexpected findings, source conflicts, or cross-topic connections discovered during research]

### Open Questions
[Agent: note any topics where sources were insufficient or conflicting]
```

---

## Scope Boundaries

**DO:**
- Fix AGENT_PLAN.md MEH-biased language (Part A)
- Update README.md file structure and status (Part B)
- Conduct web research to populate 7 knowledge base entries (Part C)
- Update research queue status (Part C2)
- Add DEVLOG Entry 10 (Part D)
- Commit and push all changes

**DO NOT:**
- Modify PLANNING_LOG.md (updated version committed alongside this directive)
- Modify any company report files (.md or .json)
- Modify company index CSVs
- Edit historical handoff files (001–007)
- Modify VISION.md or STANDARDS.md
- Change scoring methodology or weights
- Populate any knowledge base topics beyond the 7 specified
- Import claims from conversation logs — all content must come from verified external sources

## Deliverables

| File | Action |
|------|--------|
| `AGENT_PLAN.md` | Updated (mission statement + Step 3) |
| `README.md` | Updated (file structure tree + status table) |
| `knowledge/psychoacoustics/envelopment_vs_localization.md` | Created |
| `knowledge/psychoacoustics/infrasonic_perception.md` | Created |
| `knowledge/psychoacoustics/precedence_effect.md` | Created |
| `knowledge/enclosures/passive_cardioid.md` | Created |
| `knowledge/enclosures/alignment_transient_tradeoffs.md` | Created |
| `knowledge/enclosures/tapped_horn.md` | Created |
| `knowledge/acoustics/small_room_modes.md` | Created |
| `knowledge/_research_queue.md` | Updated (7 topics → populated) |
| `DEVLOG.md` | Updated (Entry 10) |
| `handoff/008_directive.md` | This file |
| `handoff/008_response.md` | Agent's completion report |

## Verification Checklist

- [ ] AGENT_PLAN.md mission statement no longer references "MEH-based system"
- [ ] AGENT_PLAN.md Step 3 reframed as topology-specific tracks (MEH as one among several)
- [ ] AGENT_PLAN.md contains no remaining instances where MEH is framed as *the* target architecture
- [ ] README.md file structure includes knowledge/, VISION.md, PLANNING_LOG.md
- [ ] README.md status table includes Directive 008
- [ ] All 7 knowledge base entries exist at specified file paths
- [ ] Each entry follows the _README.md template (Status, Confidence, Sources, Summary, Detail, Relevance, Open Questions)
- [ ] Each entry has minimum 3 source citations with resolvable URLs, DOIs, or full bibliographic references
- [ ] Each source is tagged with provenance (peer-reviewed, textbook, industry, manufacturer, community)
- [ ] No entry contains unsourced claims or content from conversation logs
- [ ] Source conflicts (if any) documented with both values
- [ ] _research_queue.md shows 7 topics as "populated"
- [ ] DEVLOG.md has Entry 10
- [ ] No company report files modified
- [ ] No historical handoff files edited
- [ ] No VISION.md or STANDARDS.md changes
- [ ] PLANNING_LOG.md not modified by agent
- [ ] Git commit and push completed
