# Sonorant Research — Planning Log

Decisions made in planning conversations (claude.ai) that affect project direction, scope, or methodology. Maintained by the planning instance and delivered alongside each directive.

This is the canonical record of *why* things were decided, not *what* was done (that's DEVLOG.md).

---

## 2025-02-05

### Transportable reclassified as preference, not constraint
**Context:** VISION.md listed "Not fixed installation — transportable" as a hard operational parameter. During review, we realized this was filtering research scope — e.g., discouraging investigation of heavy horn-loaded or concrete-baffle designs.  
**Decision:** Transportability is a design *goal*, not a research *constraint*. Reword in VISION.md to: "Transportability is valued but does not restrict research scope."  
**Rationale:** The end product should move and set up easily, but the research phase should not prematurely eliminate topologies based on weight or form factor.

### README reframed to reflect full project scope
**Context:** README still described the repo as "Research archive for boutique loudspeaker company analysis" — a framing from Directive 001. The project now spans 7 knowledge domains, 160+ companies across all segments, a vision document, and a 47-topic research queue.  
**Decision:** README rewritten to reflect actual scope. GitHub repo description should also be updated.  
**Rationale:** The old framing misrepresented the project to anyone reading the repo (including future agent instances).

### Conversation logs are archive, not active input
**Context:** `reference_raw/conversation_logs.md` (850K) served as source material for Directive 005's extraction. The structured outputs (VISION.md, _research_queue.md, DEVLOG.md) now contain everything worth preserving from those logs.  
**Decision:** Future directives reference scaffolded documents, not raw logs. The logs remain in `reference_raw/` as archive only.  
**Rationale:** Mining 850K of unstructured conversation repeatedly wastes context window and risks re-importing speculative content that was deliberately excluded.

### Context loss identified as structural risk
**Context:** Planning conversations in claude.ai exceed compaction limits during sessions that involve reviewing repo files. Decisions made early in a session can disappear before being captured anywhere.  
**Decision:** Created this PLANNING_LOG.md. The planning instance maintains it and delivers an updated version with each directive. The CLI agent replaces the file as the first step of every directive.  
**Rationale:** DEVLOG.md only captures what the CLI agent does. Planning-side decisions (scope changes, priority shifts, dropped/added requirements) had no persistent home.

### CLI agent authorized to run git commands
**Context:** Previous directives included "DO NOT run git commands — the user handles repo operations." This created unnecessary friction since the CLI agent does all the file work anyway.  
**Decision:** All future directives include git commit and push as part of deliverables.  
**Rationale:** No reason for the user to be the middleman between file creation and version control.

### Directives must be self-contained
**Context:** Context burn means the CLI agent cannot rely on having access to prior conversation history. Everything it needs must be in the directive text.  
**Decision:** Future directives include all necessary context, references, and specifications inline. No assumptions about what the agent "already knows."  
**Rationale:** Each directive may be executed by a fresh agent instance with no memory of prior work.
