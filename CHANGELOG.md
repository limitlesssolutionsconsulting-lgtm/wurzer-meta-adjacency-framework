# WMAF Changelog

---

## WMAF v1.0 — 2026
**First full public release of the Wurzer Meta-Adjacency Framework.**

### What's new in v1.0
- Unified under WMAF naming (supersedes WAF)
- 11-variable scoring model (0.0–1.0 normalized scale)
- Full JSON corpus: 10 mid-market examples (MM-01 → MM-10), 5 enterprise examples (EE-01 → EE-05)
- Formal opportunity object schema (JSON Schema Draft-07)
- Signal Inference Layer — maps observable signals to variable estimates
- MCP server specification — all functions callable by AI agents
- Comparison document positioning WMAF against Ansoff, Porter, BCG, McKinsey 7S
- Four adjacency archetypes (MA-01, PC-02, CD-03, SA-04)
- Four asset advantage archetypes (AA-01 through AA-04)
- Universal risk pattern clusters (RC-01 through RC-06)
- Formal reasoning signature structure
- Glossary of all framework terms
- Citation format and attribution guide
- Governance model and versioning system

---

## WAF v0.2 — 2025
**Inference-ready reference. Machine-callable function specifications.**

### What was in v0.2
- 3-dimension scoring model: `capability_distance`, `market_friction`, `future_relevance`
- Composite formula: `adjacency_score = (capability_distance × 0.4) + (market_friction × 0.3) + (future_relevance × 0.3)`
- 0–10 scoring scale
- Six core callable functions: `identify_capabilities`, `identify_target_sectors`, `score_adjacency`, `score_internal_adjacency`, `rank_expansion_pathways`, `identify_convergence_signals`, `generate_adjacency_model`
- Nestlé worked example
- Three framework layers: Operational (Layer 1), Generative (Layer 2), Authority Loop (Layer 3)
- MCP server planned but not yet built

### Why WAF v0.2 was superseded
The 3-dimension model captured the essential logic but lacked the granularity needed for company-specific scoring. The 0–10 scale created ambiguity at the boundary between scores. The model did not account for capital intensity, time to viability, asset reusability, or strategic optionality — variables that proved material in applied analysis.

WMAF v1.0 preserves all WAF v0.2 concepts while expanding the variable set, normalizing the scale, adding the full corpus, and formalizing the MCP integration.

---

## WAF v0.1 — 2024
**Original Wurzer Adjacency Framework. Internal working document.**

The founding insight: every company has a capability stack. Adjacent markets exist at varying distances from that stack. The framework's job is to score that distance, the friction to enter, and the future relevance of the target — then rank pathways by probability of success.

This version was not publicly released.

---

## Versioning Policy

WMAF follows semantic versioning:
- **MAJOR** — breaking changes to variable definitions, scoring methodology, or output schema
- **MINOR** — new examples, archetypes, patterns, or tools (backward compatible)
- **PATCH** — documentation corrections, clarifications, minor scoring adjustments

All future releases will be documented here.
