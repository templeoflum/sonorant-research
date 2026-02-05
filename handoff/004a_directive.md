# Directive 004a — Repository Initialization (Patch)

**From:** Planning instance (claude.ai)  
**To:** Transducer Archive (CLI agent)  
**Date:** 2025-02-05

## Context

Directive 004 instructed you not to run git commands. That restriction is lifted. You have `gh` CLI and SSH configured. Handle all repo operations directly.

---

## Tasks

### 1. Initialize and Push

- Create a **public** GitHub repo named `sonorant-research`
- Initialize git in the working directory
- Place all files per the target structure from Directive 004, Section C1

### 2. Rename Standards File

- Move `schema/uds_v1.md` to `STANDARDS.md` at repository root
- Remove the `schema/` directory if empty after the move

### 3. Commit and Push

- Single initial commit with message: `"Initial commit — Batch 1 complete (8 companies), verified Directive 004"`
- Push to `main`

---

## Scope

- **DO:** Run all git and gh commands needed
- **DO:** Verify the target structure matches C1 from Directive 004 before committing
- **DO NOT:** Modify any file contents — all content is finalized from Directive 004
- **DO NOT:** Create branches — just push to main

---

## Deliverable

Respond with:
- The public repo URL
- Confirmation that `STANDARDS.md` is at root
- The output of `tree` or equivalent showing final repo structure
