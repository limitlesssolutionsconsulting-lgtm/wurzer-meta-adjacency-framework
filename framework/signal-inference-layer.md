# Signal Inference Layer
> Version 1.0 | Wurzer Meta-Adjacency Framework

---

## Purpose

The WMAF scoring model requires 11 variable values (0.0–1.0) for each adjacency being evaluated. In human-mediated analysis, these values are assigned by a practitioner based on direct knowledge of the company. In automated or semi-automated analysis, they must be inferred from observable signals.

This document defines the **Signal Inference Layer** — the mapping between publicly observable signals and WMAF variable estimates. It is the bridge between signal detection systems (like DID and AMOS) and the WMAF scoring engine.

---

## The Signal-to-Variable Mapping

### Variable V01 — capability_distance

**Signals that indicate LOW distance (high score, 0.7–1.0):**
- Company already operates in adjacent industry (news, LinkedIn, job postings)
- Job postings mention skills directly applicable to the adjacency
- Company has acquired or partnered with players in the target space
- Leadership team has prior experience in the target sector

**Signals that indicate HIGH distance (low score, 0.0–0.3):**
- No hiring or investment in adjacent domain
- Core product is fundamentally different from adjacency requirements
- No visible crossover in technology, channels, or customer base

**Default in absence of signals:** 0.40 (partial overlap assumed)

---

### Variable V02 — customer_overlap

**Signals that indicate HIGH overlap (0.7–1.0):**
- Company serves same buyer persona as adjacent market (inferred from positioning, case studies)
- Adjacent offering is frequently purchased by same industry vertical
- Existing customer testimonials reference need for adjacent service
- Company already cross-sells loosely related offerings

**Signals that indicate LOW overlap (0.0–0.3):**
- Target market serves entirely different buyer persona
- Geographic mismatch with current customer base
- Significant procurement channel differences

**Default in absence of signals:** 0.50

---

### Variable V03 — asset_reusability

**Signals that indicate HIGH reusability (0.8–1.0):**
- Company operates physical infrastructure usable for adjacency (fleet, facilities, equipment)
- Existing technology platform directly applicable
- Recurring service routes or contracts cover same customers
- Brand and trust assets transferable to new offering

**Signals that indicate LOW reusability (0.0–0.3):**
- New offering requires entirely new infrastructure, technology, or workforce
- Brand is tightly associated with single category
- No operational overlap with adjacency requirements

**Default in absence of signals:** 0.45

---

### Variable V04 — market_proximity

**Signals that indicate HIGH proximity (0.8–1.0):**
- Adjacent market covered by same regulations or licensing requirements
- Same distribution channels serve both markets
- Industry trade associations overlap
- M&A activity connecting the two sectors in recent 24 months

**Signals that indicate LOW proximity (0.0–0.3):**
- Completely different regulatory environment
- No channel overlap
- Target market in different geographic jurisdiction

**Default in absence of signals:** 0.50

---

### Variable V05 — synergy_potential

**Signals that indicate HIGH synergy (0.8–1.0):**
- Adjacency would generate cross-sell opportunities with existing core
- Entering adjacency would strengthen defensibility of core (e.g., data flywheel)
- Shared brand benefit across both offerings
- Operational leverage clearly visible (same team, same routes, same systems)

**Signals that indicate LOW synergy (0.0–0.3):**
- Adjacency is standalone with no connection to core
- Different customer relationships required
- Separate operations with no shared infrastructure

**Default in absence of signals:** 0.45

---

### Variable V06 — scalability_index

**Signals that indicate HIGH scalability (0.8–1.0):**
- Adjacency is recurring-revenue model (subscriptions, retainers, monitoring contracts)
- Software or data component enables non-linear growth
- Existing distribution network can carry new offering
- Low incremental cost per additional customer

**Signals that indicate LOW scalability (0.0–0.3):**
- Highly labor-intensive with linear cost structure
- Geographic constraints limit expansion
- Regulatory caps on market size

**Default in absence of signals:** 0.50

---

### Variable V07 — strategic_optionality

**Signals that indicate HIGH optionality (0.8–1.0):**
- Adjacency is a platform play (builds data, relationships, or infrastructure usable elsewhere)
- Entering adjacency positions company for further adjacencies in same direction
- Provides access to new customer segments with broad purchasing power

**Signals that indicate LOW optionality (0.0–0.3):**
- Adjacency is one-off or highly specific
- Does not open further expansion paths
- Terminal market with no adjacent opportunities

**Default in absence of signals:** 0.40

---

### Variable V08 — friction_score (negative)

**Signals that indicate HIGH friction (0.7–1.0 — penalizes score more):**
- Heavy regulatory requirements (licensing, certification, compliance)
- Established incumbents with deep customer lock-in
- High barriers to switching for target customers
- News coverage of failed entrants in this space

**Signals that indicate LOW friction (0.0–0.3 — minimal penalty):**
- Fragmented market with no dominant player
- Light regulatory environment
- High customer dissatisfaction with current providers (review data, news)
- Recent entrants gaining traction quickly

**Default in absence of signals:** 0.30

---

### Variable V09 — capital_intensity (negative)

**Signals that indicate HIGH capital intensity (0.7–1.0 — penalizes score more):**
- Requires specialized equipment, facilities, or technology
- Industry benchmarks suggest high startup costs
- Company job postings for capital-intensive roles (manufacturing, heavy equipment)

**Signals that indicate LOW capital intensity (0.0–0.3 — minimal penalty):**
- Service-based adjacency requiring minimal physical investment
- Can be tested with existing team and tools
- Low inventory or infrastructure requirements

**Default in absence of signals:** 0.30

---

### Variable V10 — time_to_viability (negative)

**Signals that indicate SLOW viability (0.7–1.0 — penalizes score more):**
- Long sales cycles typical of target industry
- Certification or licensing requirements before revenue
- High customer switching costs requiring extended sales process

**Signals that indicate FAST viability (0.0–0.3 — minimal penalty):**
- Existing customers can be upsold immediately
- Offering is plug-and-play extension of current service
- Low procurement friction for target buyers

**Default in absence of signals:** 0.35

---

### Variable V11 — risk_exposure (negative)

**Signals that indicate HIGH risk (0.7–1.0 — penalizes score more):**
- Significant liability exposure (health, safety, legal, environmental)
- Regulatory uncertainty or pending changes
- High capital commitment that is difficult to reverse
- Company has limited financial cushion

**Signals that indicate LOW risk (0.0–0.3 — minimal penalty):**
- Pilot-able with minimal commitment
- Reversible if market doesn't respond
- No significant liability exposure
- Strong company balance sheet relative to required investment

**Default in absence of signals:** 0.30

---

## Automated Inference from News and Hiring Data

The DID and AMOS systems infer variable estimates using the following signal categories:

| Signal Category | Variables Primarily Affected |
|---|---|
| Leadership changes (new CEO, CRO, CTO) | V01, V07 |
| Expansion announcements | V01, V04, V07 |
| Funding rounds | V09, V11 |
| Hiring patterns (job postings by role category) | V01, V03, V08 |
| Partnership announcements | V02, V04, V05 |
| Customer review sentiment | V02, V08, V10 |
| Regulatory news | V08, V11 |
| M&A activity in adjacent sectors | V04, V07 |
| Technology platform announcements | V03, V06 |

---

## Confidence Scoring

When variable values are inferred from signals rather than direct knowledge, each variable carries a confidence score (0.0–1.0):

- **0.9–1.0** — Direct evidence (company announcement, financial disclosure)
- **0.7–0.89** — Strong inference (multiple corroborating signals)
- **0.5–0.69** — Moderate inference (single signal, reasonable extrapolation)
- **0.3–0.49** — Weak inference (proxy signals, limited data)
- **0.0–0.29** — Default assumption (no relevant signals found)

The opportunity object includes a `confidence_score` field reflecting the average confidence across all inferred variables. Low confidence scores flag outputs for human review before acting on them.

---

## Integration with n8n Workflow

The AMOS n8n engine implements this inference layer as follows:

1. **Signal ingestion** — NewsAPI, hiring data, and public filings are processed
2. **Signal classification** — each signal is tagged with the variables it affects
3. **Variable estimation** — signals are aggregated to produce variable estimates with confidence scores
4. **WMAF scoring** — estimated variables are passed to the scoring engine
5. **Opportunity object generation** — scored adjacencies are formatted as WMAF opportunity objects
6. **Human review flagging** — low-confidence outputs are flagged for practitioner review

This pipeline converts WMAF from a manual analysis tool into a semi-automated opportunity detection system while preserving the auditability and explainability of the scoring logic.

---

*For the scoring formula, see `scoring-methodology.md`. For the full variable definitions, see `variables.json`.*
