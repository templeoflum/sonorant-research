# Handoff 002 — Review & Continuation

**From:** Planning instance (claude.ai)
**To:** CLI agent (Transducer Archive)
**Date:** 2025-02-05

---

## Review of Reports 1–3

### Overall: Solid foundation. Continue with remaining 5 companies.

The Danley, Funktion-One, and Void reports are well-structured with real sources. A few corrections and improvements to apply going forward.

---

## Issues to Fix (apply retroactively when convenient, mandatory for all future reports)

### 1. Spec Provenance Tags — MISSING

The plan requires every spec to carry provenance (manufacturer|independent|derived) and confidence (high|med|low). The JSON currently has source-level confidence but individual specs don't indicate where each number came from.

**Fix:** In the JSON `key_specs` objects, add a `provenance` field per spec or a top-level `spec_provenance` note. Example:

```json
"sensitivity_db_2v83": 100,
"sensitivity_provenance": "manufacturer",
"sensitivity_confidence": "high"
```

Or at minimum, a block-level note:
```json
"spec_provenance": "All specs from manufacturer datasheets unless noted. No independent verification of sensitivity or max SPL for this model."
```

This is the single most important quality control mechanism — without it we can't distinguish what's been independently verified vs. marketing claims.

### 2. Units Normalization

Danley uses lbs/inches, Funktion-One uses kg, Void uses kg. Pick one system and stick to it across all reports. **Use metric (kg, mm) as primary** with imperial in parentheses where the manufacturer publishes in imperial. The UDS schema uses mm and kg.

### 3. Architecture-Agnostic Language

Some reports still frame analysis relative to "MEH architecture" as if it's the chosen topology (e.g., Void's relevance says "not MEH architecture" as a negative). System topology is an open variable. Score relevance against the *experiential goals* (coherence, imaging, sub-weight, fidelity, psychoacoustic potential) — not against any specific architecture.

### 4. Void Report Is Thin — Acknowledged

No patents found, no independent measurements, many product specs incomplete. This is acceptable given the company's opacity, but the audit notes should explicitly state: "Void publishes limited technical data. Many specs are marketing-level only. No third-party measurements identified." The current audit notes are close but could be more direct.

---

## Per-Report Notes

### Danley (8.54) — Strong
- Patent coverage is excellent (3 confirmed + 2 pending)
- Two independent measurement sources is the gold standard — this is what every report should aspire to
- Love Inn case study directly relevant to our scale
- Cohearix Lens (2024 provisional) is interesting for future watching
- **Minor:** SH50 composite score in handoff summary says 8.54, markdown says 8.4, JSON calculates to ~8.5. Reconcile.

### Funktion-One (7.71) — Good
- Inclusion of third-party criticism (Jumble Blue analysis) is valuable — do this for every company where independent critique exists
- Tony Andrews claimed to have 8+ patents but only 1 found (US6650760B1). Note this gap explicitly: "Manufacturer claims 8+ patents; only 1 confirmed via Google Patents. Justia returned 403."
- The "no-EQ" philosophy is genuinely interesting as a design constraint to study, not just a marketing claim

### Void (6.43) — Adequate
- Honest about the data gaps, which is correct behavior
- DC10 replacement by Loud Professional is a useful competitive signal
- Fibreglass construction technique is the main R&D takeaway worth deeper study in Track B (Enclosures)

---

## Directive: Continue Batch 1 (Companies 4–8)

Proceed with:
4. **KV2 Audio** — Focus on point-source coherence, transient performance, their "no line array" philosophy
5. **Fulcrum Acoustic** — Coaxial designs, passive cardioid technology, pattern control
6. **PK Sound** — Robotic line source, variable beam steering, Trinity platform
7. **HOLOPLOT** — 3D audio beamforming, wave field synthesis, X1 matrix array
8. **Hennessey Sound Systems** — Expect limited data. Document what's findable, flag as thin.

### Apply These Standards Going Forward:
- Spec provenance on every number (even if just a block-level note)
- Metric primary, imperial parenthetical
- Score against experiential goals, not any assumed topology
- Include third-party criticism where it exists
- Be explicit about data gaps in audit notes

### After Batch 1 Completion:
Write a `handoff/002_response.md` with:
1. Status table (all 8 companies)
2. Cross-company comparison table (update the sub architecture comparison from 001_response to include all 8)
3. Any emerging patterns or surprises
4. Questions for the planning instance if any

Do NOT start Batch 2 without a directive. We'll review the full pilot set first.
