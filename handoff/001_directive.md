# Handoff 001 — Initial Directive

**From:** Planning instance (claude.ai)
**To:** CLI agent (Transducer Archive)
**Date:** 2025-02-04

## Context

You are Transducer Archive, a research agent. Read `AGENT_PLAN.md` and `schema/uds_v1.md` thoroughly before starting any work. The README.md at repo root contains your operating instructions.

## Task: Pilot Batch — Boutique Systems (8 companies)

Run the full per-company pipeline (AGENT_PLAN.md Part 3) on these 8 companies in order:

1. **Danley Sound Labs** — Highest priority. The Synergy Horn is the ancestral technology behind Sonorant's MEH approach. We need the patent lineage, all Synergy Horn variants, Tapped Horn sub patents, and any AES papers by Tom Danley.
2. **Funktion-One** — Tony Andrews' acoustic-first philosophy. Focus on their horn designs, driver choices, and the "no corrective EQ" approach.
3. **Void Acoustics** — Aesthetic + engineering fusion. Fiberglass horn construction, multi-horn stacks.
4. **KV2 Audio** — Known for point-source coherence and transient performance. Relevant to our MEH goals.
5. **Fulcrum Acoustic** — Coaxial designs, pattern control.
6. **PK Sound** — Robotic line source, beam steering.
7. **HOLOPLOT** — 3D beamforming arrays, wave field synthesis.
8. **Hennessey Sound Systems** — Underground/boutique, limited info expected.

## Output Per Company

For each company, produce:
- `reports/boutique/<company_id>.md` — Markdown dossier per template in UDS Section 11
- `reports/boutique/<company_id>.json` — JSON sidecar per UDS schema
- Append rows to `reports/_indexes/companies.csv` and `reports/_indexes/models.csv`

## Special Emphasis for This Batch

Given Sonorant's MEH + sub architecture, pay extra attention to:
- Any multi-entry horn, synergy horn, or unity horn implementations
- Tapped horn and horn-loaded sub designs
- Point-source coherence mechanisms
- Phase/time alignment approaches
- Patents related to horn geometry, driver summation in shared horns, or waveguide design
- Case studies in 100–300 cap venues (clubs, theaters, small festivals)

## Quality Reminders

- Every spec needs provenance (manufacturer|independent|derived) and confidence (high|med|low)
- Every non-obvious claim needs a resolvable URL
- Use `null` for unknown, never guess
- If you can't find ≥5 sources for a company, write an audit note explaining why
- Flag when manufacturer claims differ from independent measurements

## Questions?

If you hit design-priority ambiguity or need clarification, write to `handoff/001_response.md` and pause that company. The human will relay to the planning instance.
