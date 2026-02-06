# Sonorant Research — Planning Log

The canonical record of current project decisions and their rationale. Organized by domain, not chronology. Each section shows what's currently true, why, and when it changed.

For the chronological record of what was done, see DEVLOG.md.

Maintained by the planning instance and delivered alongside each directive. The CLI agent replaces this file as the first step of every directive.

---

## Scope & Constraints

### Research Scope

**Current:** Research spans 7 knowledge domains, 160+ companies across all market segments, and a 47-topic research queue. No topology, architecture, or form factor is pre-excluded from investigation. System architecture is explicitly OPEN — determined by research, not assumption.

**Rationale:** The experiential goals are locked; the physical means of achieving them are not. Premature filtering based on assumptions about weight, size, complexity, or preferred topology would eliminate potentially optimal solutions.

| Directive | Date | Change |
|-----------|------|--------|
| 008 | 2025-02-05 | AGENT_PLAN.md cleaned of MEH-biased language in mission statement and research tracks; architecture-agnostic stance now consistent across all documents |
| 006 | 2025-02-05 | README rewritten to reflect full scope (was "boutique loudspeaker analysis") |
| 005 | 2025-02-05 | Knowledge base scaffolded across 7 domains; research queue extracted |
| 001 | 2025-02 | Initial framing focused on boutique company research |

### Transportability

**Current:** Transportability is a design goal, not a research constraint. The end product should move and set up easily, but research does not exclude topologies based on weight or form factor.

**Rationale:** Listing transportability as a hard constraint was filtering research scope — discouraging investigation of heavy horn-loaded or concrete-baffle designs that might offer superior acoustic performance.

| Directive | Date | Change |
|-----------|------|--------|
| 006 | 2025-02-05 | Reclassified from constraint to preference |
| 005 | 2025-02-05 | Initially extracted as hard operational parameter |

### Venue Scale

**Current:** 100–200 person capacity. Small rooms, outdoors, portable contexts. This is a hard constraint — the system is designed for intimate communal gatherings, not festival scale.

**Rationale:** Core experiential intent. Not subject to revision.

| Directive | Date | Change |
|-----------|------|--------|
| 005 | 2025-02-05 | Extracted from conversation logs; confirmed by project owner |

---

## Sonic Priorities

**Current:** Five co-equal constraints that define the design space simultaneously. None is ranked above another — the system must satisfy all five. They are the shape of the box, not a stack inside it.

1. Psychoacoustic immersion
2. Sub weight (infrasonic extension)
3. Hyper-real clarity
4. Fast transients
5. Small-room optimization

**Rationale:** Ranking implied acceptable tradeoffs that don't exist. A design that sacrifices one for another has failed. The scoring weights (0.23/0.23/0.23/0.20/0.11) are used for R&D relevance scoring of company reports only — they do not imply experiential priority.

| Directive | Date | Change |
|-----------|------|--------|
| 007 | 2025-02-05 | Removed ranking; presented as co-equal constraints |
| 005 | 2025-02-05 | Initially extracted as ranked list from conversation logs |

---

## Aesthetic Identity

**Current:**
- **Ethos:** Sonic liberation — sound as force, presence, and freedom
- **Visual language:** Transduction instrumentation — physics-driven form, material honesty, exposed function as the only ornament
- **Palette:** Oscilloscope lineage (Tektronix Gray, Bakelite Black, natural wood, brushed metal, functional indicators)
- **System animacy:** Presence earned through modular evolution, operator relationship, acoustic interaction, and accumulated collective experience — not through narrative or branding

**Rationale:** Sonorant's aesthetic should emerge from its own substrate (air pressure, physical material) rather than borrowing from digital or mythological domains. The animacy concern is preserved and grounded: the system develops character through use, not through being declared sacred.

**Explicitly rejected:**
- "Mythopoetic" — carries 1980s–90s men's movement associations
- "Mythogenetic" — belongs to a separate project (MythOS); conflates distinct creative domains
- "Sonic entity," "transcension engine," "sonic activation" — narrative framing that doesn't belong here
- Decorative sacred geometry, themed/costumed design, vaporwave/retro-futurist/cyberpunk aesthetics

| Directive | Date | Change |
|-----------|------|--------|
| 007 | 2025-02-05 | Complete overhaul: replaced mythic framing with sonic liberation / transduction instrumentation framework; added "System as Evolving Instrument" concept |
| 005 | 2025-02-05 | Initial extraction inherited "glitchy mythopoetic cyber surrealism" from ChatGPT-era conversation logs |

---

## Scoring Methodology

**Current:** 5-criterion R&D relevance scoring system with weights:

- hf_clarity_transient: 0.23
- directivity_control_imaging: 0.23
- sub_weight_infrasonic: 0.23
- psychoacoustic_potential: 0.20
- small_room_viability: 0.11

Scores evaluate company/product relevance to Sonorant's goals. They do not imply priority ranking among experiential goals. All rationale must connect specs to experiential outcomes, not to assumed topologies.

**Rationale:** Original 6-criterion system included modularity_transport, which biased toward specific architectures. Scoring must be architecture-agnostic.

| Directive | Date | Change |
|-----------|------|--------|
| 007 | 2025-02-05 | Clarified that weights are for scoring only, not experiential priority |
| 004 | 2025-02-05 | UDS updated to v1.1; verified all reports use consistent weights |
| 003 | 2025-02-05 | Score recalculation pass; corrected rounding errors |
| 002 | 2025-02 | Dropped modularity_transport criterion; redistributed to 5-criterion system |
| 001 | 2025-02 | Initial 6-criterion system established |

---

## Source Material & Verification

### Conversation Logs

**Current:** `reference_raw/conversation_logs.md` is archive only. Future directives reference scaffolded documents (VISION.md, _research_queue.md, knowledge base), not raw logs.

**Rationale:** The logs contain extensive ChatGPT-generated content that cannot be trusted. Structured outputs now contain everything worth preserving. Re-mining 850K of unstructured conversation wastes context and risks re-importing speculative content.

| Directive | Date | Change |
|-----------|------|--------|
| 006 | 2025-02-05 | Logs reclassified as archive; scaffolded documents are canonical |
| 005 | 2025-02-05 | Vision and research queue extracted from logs |

### Verification Standards

**Current:** Every claim in the knowledge base requires:
- Source citation (resolvable URL, DOI, or full bibliographic reference + date)
- Provenance tag (peer-reviewed | textbook | industry | manufacturer | community)
- Confidence rating (high | med | low)

Manufacturer claims vs. independent measurements must be distinguished. Conflicts documented with both values.

**Rationale:** Early ChatGPT sessions contained numerous hallucinated specs and fabricated citations. Strict verification prevents contamination.

| Directive | Date | Change |
|-----------|------|--------|
| 008 | 2025-02-05 | Provenance tags expanded from 3-tier to 5-tier (peer-reviewed, textbook, industry, manufacturer, community) for knowledge base entries |
| 005 | 2025-02-05 | Knowledge base entry standards established |
| 002 | 2025-02 | Spec provenance tagging added to methodology |
| 001 | 2025-02 | Hallucination problem identified; quarantine established |

---

## Process Norms

### Directive Structure

**Current:** Directives are fully self-contained. All necessary context, references, and specifications are inline. No assumptions about what the agent "already knows."

**Rationale:** Context burn means the CLI agent cannot rely on prior conversation history. Each directive may be executed by a fresh agent instance.

| Directive | Date | Change |
|-----------|------|--------|
| 006 | 2025-02-05 | Self-containment requirement formalized |

### Git Operations

**Current:** CLI agent is authorized to commit and push. Git operations are included as part of directive deliverables.

**Rationale:** No reason for the user to be the middleman between file creation and version control.

| Directive | Date | Change |
|-----------|------|--------|
| 006 | 2025-02-05 | Agent authorized for git operations |
| Prior | — | User handled all repo operations manually |

### Planning Log Maintenance

**Current:** This file is maintained by the planning instance and delivered alongside each directive. The CLI agent replaces the file as the first step of every directive. Organized by domain with history tables, not chronological append-only.

**Rationale:** DEVLOG.md captures what the CLI agent does. Planning-side decisions (scope changes, priority shifts, reclassifications) need a persistent home that shows current state clearly, with superseded decisions tracked in history rather than cluttering the main view.

| Directive | Date | Change |
|-----------|------|--------|
| 007 | 2025-02-05 | Restructured from chronological to domain-based organization |
| 006 | 2025-02-05 | PLANNING_LOG.md created |

### Knowledge Base Population

**Current:** The knowledge base is populated in batches selected for foundational relevance — topics that other research builds on are prioritized first. Each batch is scoped in a directive with specific topic assignments, source requirements, and verification standards.

Entry requirements:
- Follows the template in each directory's `_README.md`
- Minimum 3 sources per entry, preferring peer-reviewed and textbook sources
- Every source tagged with provenance (peer-reviewed | textbook | industry | manufacturer | community)
- Source conflicts documented with both values and provenance
- Unknown = "not established" — never estimated or inferred
- No content from conversation logs; all material from verified external sources

**Rationale:** The knowledge base was scaffolded in Directive 005 but remained empty. Population order matters — foundational topics (psychoacoustic principles, enclosure physics, room behavior) must be established before design synthesis can draw on them meaningfully.

| Directive | Date | Change |
|-----------|------|--------|
| 008 | 2025-02-05 | First population batch: 7 topics across psychoacoustics, enclosures, and acoustics |
| 005 | 2025-02-05 | Knowledge base scaffolded; 47-topic research queue created |
