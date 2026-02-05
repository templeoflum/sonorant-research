# Directive 006 — Process Fixes & Planning Log Introduction

**From:** Planning instance (claude.ai)  
**To:** Transducer Archive (CLI agent)  
**Date:** 2025-02-05

## Objective

Introduce the planning log as a persistent record of planning-side decisions, fix the transportability classification in VISION.md, and establish updated process norms for all future directives. This is a housekeeping directive — no new research, no knowledge base population.

---

## PART A: Add PLANNING_LOG.md

### A1. Place the file

The attached `PLANNING_LOG.md` is provided alongside this directive. Place it at the repo root:

```
sonorant-research/PLANNING_LOG.md
```

This file is maintained by the planning instance (claude.ai) and delivered as an updated version with each future directive. The CLI agent's only responsibility is to **replace the existing file** with the version provided — never edit it independently.

### A2. Purpose

The planning log captures decisions made in planning conversations that affect project direction, scope, or methodology. It records *why* things were decided. DEVLOG.md records *what* was done. They are complementary.

---

## PART B: Update VISION.md

### B1. Reclassify transportability

In VISION.md, Section 3 (Operational Parameters), find:

```
Not fixed installation — transportable
```

Replace with:

```
Transportability is valued but does not restrict research scope — the end product should move and set up easily, but research should not prematurely eliminate topologies based on weight or form factor
```

No other changes to VISION.md.

---

## PART C: Update DEVLOG.md

Add Entry 8:

```
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
```

---

## PART D: Update README.md

In the "Key Documents" table at the bottom of README.md, add a row:

```
| `PLANNING_LOG.md` | Why decisions were made — planning-side rationale and scope changes |
```

In the "Project Structure" tree, add `PLANNING_LOG.md` at the root level alongside the other top-level files:

```
├── PLANNING_LOG.md              # Planning-side decisions and rationale
```

In the "Current Status" table, add:

```
| 006 | Process fixes + planning log introduction | ✅ Complete |
```

---

## PART E: Git Operations

Commit all changes with the message:

```
Directive 006 — Process fixes, planning log, transportability reclassification
```

Push to main.

---

## Scope Boundaries

**DO:**
- Place the provided PLANNING_LOG.md at repo root
- Update VISION.md (transportability line only)
- Update DEVLOG.md with Entry 8
- Update README.md (key documents table, project structure, status table)
- Commit and push

**DO NOT:**
- Edit PLANNING_LOG.md beyond placing it (it is maintained by the planning instance)
- Modify any report files, knowledge base files, or research queue
- Conduct any research or web lookups
- Edit historical handoff files (001–005)

---

## Deliverables

| File | Action |
|------|--------|
| `PLANNING_LOG.md` | New file (provided) |
| `VISION.md` | Updated (transportability line) |
| `DEVLOG.md` | Updated (Entry 8) |
| `README.md` | Updated (key docs, structure, status) |
| `handoff/006_directive.md` | This file |
| `handoff/006_response.md` | Agent's summary of changes |
| Git commit + push | Required |

---

## Verification Checklist

- [ ] PLANNING_LOG.md exists at repo root and matches the provided version exactly
- [ ] VISION.md transportability line updated, no other changes
- [ ] DEVLOG.md has Entry 8
- [ ] README.md key documents table includes PLANNING_LOG.md
- [ ] README.md project structure includes PLANNING_LOG.md
- [ ] README.md status table includes Directive 006
- [ ] No report files, knowledge base files, or research queue modified
- [ ] No historical handoff files edited
- [ ] Changes committed and pushed to main
