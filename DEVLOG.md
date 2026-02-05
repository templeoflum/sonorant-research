# Sonorant Research — Development Log

Chronological, append-only record of decisions, rationale, and findings.

---

## Entry 1 — Project Inception

**Date:** 2025-02 (early)
**Phase:** Initial setup

### What Happened
- Distilled raw conversation material (ChatGPT sessions) into structured research plan
- Created Uniform Data Standard (UDS) v1.0 specification
- Defined 5-criterion R&D relevance scoring system
- Selected pilot batch of 8 boutique companies

### Key Decisions and Rationale
- **Company selection rationale:** Intentional mix across multiple dimensions:
  - **Established:** Danley Sound Labs, Funktion-One (proven track records, extensive documentation)
  - **Emerging:** Fulcrum Acoustic, KV2 Audio (newer companies with interesting technology)
  - **Scale contrast:** HOLOPLOT (massive venue-scale WFS), PK Sound (festival robotics)
  - **Aesthetic:** Void Acoustics (design-forward, club market)
  - **Niche:** HSD (bass culture, festival circuit)
- **Why boutique over majors:** Boutique manufacturers often publish more technical detail and are more willing to discuss design decisions. Major manufacturers (d&b, L-Acoustics, Meyer) can serve as comparison baselines in later batches.
- **UDS design:** Schema prioritizes source provenance, confidence tagging, and distinguishing manufacturer claims from independent measurements.

### Surprises or Pattern Shifts
- Raw conversation logs from prior ChatGPT sessions contained numerous hallucinated specs and fabricated citations. Decision: quarantine in `reference_raw/` and mark as unverified.

### Open Questions
- Optimal scoring weights for the 5-criterion system
- Whether to include modularity/transport as a criterion

---

## Entry 2 — Batch 1, First Half (Directive 001)

**Date:** 2025-02
**Phase:** Directive 001

### What Happened
- Completed deep-dive reports: Danley Sound Labs, Funktion-One, Void Acoustics
- Established research methodology and source requirements

### Key Decisions and Rationale
- **Danley emerged as anchor:** Only company with multiple independent third-party measurements (Erin's Audio Corner Klippel NFS, Merlijn van Veen live venue). This became the gold standard for the dataset.
- **Funktion-One established as bass culture reference:** Strong EDM/club presence, documented "audio moment" philosophy, but limited independent verification.
- **Void flagged as aesthetic-only:** Thin on verifiable tech despite visual appeal. No patents found despite claimed innovations (HTT, Pressure Gradient Porting).

### Surprises or Pattern Shifts
- Initial scoring inadvertently used MEH (Multi-Entry Horn) as implicit benchmark, biasing scores toward that topology.
- Patent verification harder than expected — manufacturer claims don't always match USPTO/Google Patents records.

### Open Questions
- How to score companies fairly without assuming a specific topology?
- Should the scoring system include architecture-specific criteria?

---

## Entry 3 — Course Correction (Directive 002)

**Date:** 2025-02
**Phase:** Directive 002 (methodology update)

### What Happened
- Identified three systematic issues:
  1. No spec provenance tagging
  2. Imperial-first units
  3. MEH-biased scoring rationale
- Updated methodology for remaining companies

### Key Decisions and Rationale
- **Score against experiential goals, not assumed topology:** Changed scoring rationale to reference clarity, imaging, sub-weight, psychoacoustic impact, and small-room viability rather than proximity to any specific architecture.
- **Dropped `modularity_transport` criterion:** Too architecture-specific. A point source doesn't need modularity the way a line array does.
- **Redistributed weights to 5-criterion system:**
  - hf_clarity_transient: 0.23
  - directivity_control_imaging: 0.23
  - sub_weight_infrasonic: 0.23
  - psychoacoustic_potential: 0.20
  - small_room_viability: 0.11
- **Metric-first units:** All specs normalized to `XX kg (YY lbs)` format.
- **Spec provenance requirement:** Every product table must have a provenance note.

### Surprises or Pattern Shifts
- Realizing that the scoring rationale was inadvertently measuring "how MEH-like is this?" rather than "how well does this serve the experiential goals?"

### Open Questions
- How to bring Batch 1 first-half reports (Danley, Funktion-One, Void) to the new standard?

---

## Entry 4 — Batch 1, Second Half (Directive 002 continued)

**Date:** 2025-02
**Phase:** Directive 002 (continued research)

### What Happened
- Completed deep-dive reports: KV2 Audio, Fulcrum Acoustic, PK Sound, HOLOPLOT, HSD

### Key Decisions and Rationale
- Applied updated methodology from Entry 3
- All new reports include spec provenance, metric-first units, architecture-agnostic rationale

### Key Findings

1. **Fulcrum's passive cardioid patent (US10,123,111 B2):** Most directly relevant innovation for small-room sub design. Achieves directional LF control mechanically without active arrays.

2. **Directivity control spectrum emerged:**
   - Mechanical-acoustic (Danley Synergy Horn, Funktion-One horns)
   - Mechanical-robotic (PK Sound Trinity)
   - DSP-hybrid (Fulcrum TQ)
   - Full DSP (HOLOPLOT WFS + beamforming)

3. **Patent claims vs. reality gap:** "Proprietary" often means trade secret, not patented. Multiple companies claim patent-pending technologies with no granted patents found.

4. **Only Danley has independent measurements:** Single biggest differentiator in dataset. All other companies rely entirely on manufacturer claims.

5. **HOLOPLOT Sphere acquisition:** May affect commercial availability and product direction. Technology impressive but optimized for venue-scale, not small rooms.

6. **Small-room suitability ranking crystallized:** Fulcrum, Danley, KV2 as top three based on product scale, weight, and design intent.

### Surprises or Pattern Shifts
- HSD's "Burning Man durability" benchmark an interesting proxy for build quality
- Festival/touring vs. install market segmentation more pronounced than expected

### Open Questions
- None critical — ready for correction pass

---

## Entry 5 — Correction Pass (Directive 003)

**Date:** 2025-02-05
**Phase:** Directive 003

### What Happened
- Brought Danley, Funktion-One, Void to Batch 2 standard
- All three composite scores were recalculated and corrected

### Key Decisions and Rationale
- **Recalculated all scores:** Found rounding errors in original calculations
  - Danley: 8.54 → 8.58
  - Funktion-One: 7.71 → 7.78
  - Void: 6.43 → 6.55
- **Removed MEH reference from Void:** Changed "not MEH architecture" to architecture-neutral language
- **Added spec provenance notes:** All product tables now have provenance statements
- **Standardized audit notes format:** Consistent structure across all reports

### Surprises or Pattern Shifts
- All three original composite scores contained calculation errors

### Open Questions
- Do the remaining 5 reports (KV2, Fulcrum, PK, HOLOPLOT, HSD) also have score calculation errors?

---

## Entry 6 — Verification & Repository Setup (Directive 004)

**Date:** 2025-02-05
**Phase:** Directive 004

### What Happened
- Verified composite scores across all 8 reports
- Found and fixed 3 additional calculation errors (KV2, Fulcrum, PK Sound)
- Found STANDARDS.md (schema/uds_v1.md) still had old 6-criterion scoring system
- Updated standards to match actual practice (UDS v1.0 → v1.1)
- Set up repository structure for version tracking
- Created indexes for filtering (companies.csv, models.csv)

### Key Decisions and Rationale
- **Fixed score calculation errors:**
  - KV2: 7.82 → 7.77
  - Fulcrum: 8.02 → 8.00
  - PK Sound: 6.64 → 6.79
- **Updated UDS to v1.1:** Removed modularity_transport criterion, updated weights to 5-criterion system, removed architecture-specific R&D flags (transport_modular, synergy_candidate).
- **Fixed Danley rationale:** small_room_viability now uses metric-first: "SM60F at 22.7 kg (50 lbs)"

### Surprises or Pattern Shifts
- STANDARDS.md had drifted from actual practice — spec said 6 criteria with different weights, but all reports used 5 criteria with current weights.
- 5 of 8 composite scores had calculation errors > 0.01

### Open Questions
- None — dataset now at parity

---

## Batch 1 Final Summary

**Companies Researched:** 8
**Reports Complete:** 8 markdown + 8 JSON
**Average Composite Score:** 7.29/10

**Top 3 for Small-Room Viability:**
1. Fulcrum Acoustic (8/10) — passive cardioid patent, TQ processing, installation focus
2. KV2 Audio (8/10) — ESD series compact, trans-coil technology
3. Danley Sound Labs (7/10) — SM60F validated, Love Inn case study

**Key Technology Findings:**
- Passive cardioid (US10,123,111 B2) most directly applicable to Sonorant sub design
- Independent measurements remain the gold standard — only Danley has them
- Patent verification essential — claims frequently exceed verifiable reality

**Ready for Batch 2.**

---

## Entry 7 — Vision Extraction & Knowledge Base Scaffolding (Directive 005)

**Date:** 2025-02-05
**Phase:** Directive 005

### What Happened
- Extracted Sonorant Sound vision from conversation logs into VISION.md
- Created knowledge base directory structure with entry templates and standards
- Built research queue from conversation logs — extracted topics, not answers
- Established three-layer triage for conversation log material:
  - Vision statements → import to VISION.md
  - Research questions → queue in _research_queue.md
  - Speculative design output → leave in reference_raw/

### Key Decisions and Rationale
- **Vision document is statement of intent, not spec:** VISION.md captures experiential goals and design parameters without importing unverified technical claims.
- **Knowledge base starts empty:** Directory structure with templates in place, but no content populated. This ensures all future entries meet source verification standards.
- **Research queue extracts questions, not answers:** 47 topics identified for future verified research, organized by category and priority.

### Extracted Statistics
- **Topics extracted:** 47 across 7 categories
- **Priority distribution:** 21 high, 20 medium, 6 low
- **Category breakdown:** psychoacoustics (8), enclosures (12), transducers (9), acoustics (5), signal_processing (6), materials (3), references (4)

### Notable Patterns Found
- Psychoacoustics and enclosures dominate the research queue — aligns with Sonorant's experiential focus
- Many topics reference the same foundational sources (Beranek, Leach, Klippel, Toole)
- Passive cardioid design appears in multiple contexts (company research + knowledge queue)
- Clear emphasis on small-room behavior throughout logs

### Surprises or Pattern Shifts
- Conversation logs contain extensive ChatGPT-generated "research" that cannot be trusted — substantial volume of plausible-sounding but unverified technical content
- Vision statements are fairly consistent across logs; no major contradictions found
- The "100-200 cap" venue scale appears repeatedly as a hard constraint

### Open Questions
- Research queue priorities need user review and confirmation
- VISION.md sonic priority ranking flagged as [NEEDS CONFIRMATION]
- Symbolic identity / naming decisions still open

---

## Entry 8 — Process Fixes & Planning Log (Directive 006)

**Date:** 2025-02-05
**Phase:** Directive 006

### What Happened

- Introduced PLANNING_LOG.md as persistent record of planning-side decisions
- Updated VISION.md to reclassify transportability as preference, not constraint
- Established updated process norms: git operations included in directives, directives are self-contained, conversation logs are archive only

### Key Decisions and Rationale

- **Planning log introduced:** DEVLOG.md only captures CLI agent actions. Decisions made in planning conversations (scope changes, priority shifts, reclassifications) had no persistent home. PLANNING_LOG.md fills this gap. It is maintained by the planning instance and delivered alongside each directive.
- **Transportability reclassified:** "Not fixed installation — transportable" was listed as a hard constraint in VISION.md. This was restricting research scope by implicitly filtering out heavy or fixed-installation designs. Reclassified as a design goal that does not limit the research phase.
- **Process norms formalized:** CLI agent now authorized to commit and push. Directives are self-contained (no assumed prior context). Conversation logs in reference_raw/ are archive material — structured documents are canonical.

### Surprises or Pattern Shifts

None — this is purely process housekeeping.

### Open Questions

None.
