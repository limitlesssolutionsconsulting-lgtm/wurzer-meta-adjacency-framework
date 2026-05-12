# Wurzer Meta-Adjacency Framework (WMAF)
> Version 1.0 — Inference-Ready Reference  
> Author: Warren Wurzer, Limitless Solutions Consulting  
> Contact: info@limitlesssolutionsconsulting.com  
> Origin: Kelowna, British Columbia, Canada

---

## What This Is

The **Wurzer Meta-Adjacency Framework (WMAF)** is a structured reasoning system for identifying, scoring, and ranking adjacent market opportunities for mid-market and enterprise companies.

It is designed to be:
- **Machine-callable** — functions with defined inputs and outputs, not prose
- **Agent-compatible** — modular, parametric, and simulation-ready
- **Ontologically clean** — every term formally defined, every variable bounded
- **Meta-generative** — a system for producing adjacency logic on demand, not just one instance of it

WMAF is the reasoning backbone of two operational systems:
- **DID (Daily Intelligence Distributor)** — automated signal detection pipeline
- **AMOS (Adjacent Market Opportunity Scanner)** — strategic analysis tool

---

## The Problem This Solves

Organizations that operate in a particular market long enough tend to lose objectivity about it. This is not a failure of intelligence — it is the natural outcome of success.

Operational pressure, internal alignment, investor expectations, legacy systems, and the day-to-day demands of running a business gradually narrow the field of vision. Strategic assumptions become normalized. Markets that are saturated, over-optimized, or structurally constrained begin to feel like the only markets that exist.

There is also a broader psychological dynamic at play. Businesses can become so accustomed to the conditions surrounding them that subtle market shifts, behavioral changes, emerging adjacencies, or early-stage threats fail to register with the urgency they deserve — a phenomenon not unlike the proverbial frog in the frying pan. The change is gradual enough that it becomes difficult to perceive from within.

As a result, many organizations continue applying pressure to familiar channels and familiar strategies, even as the surrounding landscape quietly evolves.

> **This is one of the most common and least discussed challenges in business. Almost every business owner faces it.**

The Wurzer Meta-Adjacency Framework exists to restore that objectivity — systematically, and without requiring the owner to already know where to look.

**WMAF is the structured solution to that structural problem.**

---

## How WMAF Differs from Existing Frameworks

See [`COMPARISON.md`](./COMPARISON.md) for a detailed breakdown. The short version:

| Framework | Output | Machine-Readable | Scores Specific Opportunities | Explains Reasoning |
|---|---|---|---|---|
| Ansoff Matrix | 4 quadrant labels | No | No | No |
| Porter's Five Forces | Industry pressure map | No | No | No |
| BCG Matrix | Portfolio categories | No | No | No |
| McKinsey 7S | Alignment checklist | No | No | No |
| **WMAF** | **Ranked, scored, reasoned opportunity objects** | **Yes** | **Yes** | **Yes** |

---

## Target User

**Primary:** Founders and owners of companies generating $5M–$500M in annual revenue.

- The owner is close enough to the business to be its greatest asset and its greatest blind spot simultaneously
- The company is large enough to have real capabilities worth leveraging
- The company is small enough that a single well-identified adjacency can be transformational
- Strategic consultants at this level are expensive and often generalist — WMAF provides structured, specific, actionable output

**Secondary:** Advisors, M&A brokers, PE firms, enterprise strategy teams, and AI agents performing expansion analysis.

---

## Core Premise

Every company has a set of existing capabilities. Adjacent markets exist at varying distances from those capabilities. The framework scores that distance, the friction to enter, and the future relevance of the target market — then ranks expansion pathways by probability of success.

> **The fundamental insight:** Opportunity is not about where a company wants to go. It is about where their existing capabilities can reach with the least friction, in a market that is growing toward them.

Adjacency operates in two directions:

**External adjacency** — new markets, sectors, or customer segments the company's existing capabilities can serve with minimal adaptation.

**Internal adjacency** — opportunities already inside the current business. The most common form: what are existing customers already buying elsewhere that this company could provide? The trust relationship already exists. The revenue is going to someone else.

---

## Repository Structure

```
wmaf-repo/
│
├── README.md                          ← You are here. Start here.
├── COMPARISON.md                      ← WMAF vs. existing frameworks
├── CITATION.md                        ← How to cite WMAF
├── GLOSSARY.md                        ← Formal definitions of all terms
├── CHANGELOG.md                       ← Version history (WAF → WMAF)
├── LICENSE                            ← Proprietary, all rights reserved
│
├── /framework                         ← The core reasoning engine
│   ├── core-logic.md                  ← Foundational principles
│   ├── variables.json                 ← Canonical variable definitions
│   ├── scoring-methodology.md         ← Weighted scoring model
│   ├── transformation-pipeline.md     ← How variables become scores
│   ├── decision-tree.md               ← Gate logic for viability
│   ├── opportunity-object-schema.json ← Canonical output schema
│   └── signal-inference-layer.md      ← How signals map to variables
│
├── /meta                              ← Cross-industry pattern library
│   ├── adjacency-archetypes.md        ← 4 universal adjacency patterns
│   ├── asset-advantage-archetypes.md  ← 4 structural leverage types
│   ├── risk-patterns.md               ← Universal friction clusters
│   ├── reasoning-signatures.md        ← Explainability framework
│   └── meta-analysis.md               ← Cross-corpus pattern synthesis
│
├── /examples
│   ├── /mid-market                    ← MM-01 through MM-10 (JSON)
│   └── /enterprise                    ← EE-01 through EE-05 (JSON)
│
├── /schema                            ← Machine-readable ontology
│   ├── wmaf-schema.json               ← JSON Schema (Draft-07)
│   └── wmaf-ontology.yaml             ← YAML ontology definition
│
└── /mcp                               ← MCP server specification
    ├── README.md                      ← MCP integration guide
    └── tool-definitions.json          ← Callable tool specifications
```

---

## The Six Multiplier Dimensions

Every adjacency WMAF identifies belongs to one or more of these dimensions:

| Dimension | Description |
|---|---|
| **Asset Generation** | Identifying underutilized assets — relationships, infrastructure, knowledge, geography — and converting them into revenue streams |
| **Profitability Improvement** | Finding where margin is structurally lost and redesigning the model to capture it |
| **Higher Margin Opportunities** | Adjacent products, services or markets with better economics than the core business |
| **Quality Improvement** | Elevating the offer so price resistance drops and client retention increases |
| **Product Advancement** | Expanding what the business sells without building from scratch — using existing capability differently |
| **Adjacent Market Expansion** | Entering complementary markets where existing assets create an unfair advantage over new entrants |

> **Cost-cutting makes something smaller. Adjacency makes something more. The goal is multiplication, not subtraction.**

---

## Core Scoring Functions

### `identify_capabilities(company)`
Extracts the company's core capability stack relevant to adjacency analysis.

**Output fields:** `capability_id`, `capability_name`, `transferability_score` (0–1), `defensibility_score` (0–1)

---

### `score_adjacency(capability_stack, target_sector)`
The core scoring function. Returns a structured adjacency score for one capability stack against one target sector.

**Three primary scoring dimensions:**

| Dimension | Description | Scale |
|---|---|---|
| `capability_distance` | How much of the existing stack transfers directly | 0–1 (1 = direct transfer) |
| `market_friction` | Regulatory barriers, competition, capital requirements | 0–1 (1 = near-zero friction) |
| `future_relevance` | Sector growth trajectory toward the company | 0–1 (1 = inevitable convergence) |

**Composite Score:**
```
adjacency_score = Σ(weight_i × variable_i)
```

Full variable set and weights defined in `/framework/variables.json`.

---

### `score_internal_adjacency(company)`
Identifies revenue opportunities already inside the business by analyzing the gap between what existing customers buy from this company and what they purchase elsewhere.

**Core question:** *What are this company's existing customers going elsewhere to buy that this company could reasonably provide?*

---

### `generate_adjacency_model(company, context)`
Meta-layer function. Generates a complete, custom adjacency model for any company/context combination on demand. Calls all scoring functions internally and returns a full structured opportunity object.

---

## Verdict Thresholds

| Composite Score | Verdict |
|---|---|
| 0.76 – 1.00 | **Top adjacency** — high conviction expansion pathway |
| 0.63 – 0.75 | **Strong adjacency** — viable with strategic investment |
| 0.50 – 0.62 | **Moderate adjacency** — possible but not priority |
| 0.35 – 0.49 | **Weak adjacency** — resource intensive, low ROI |
| 0.00 – 0.34 | **Not recommended** — structural mismatch |

---

## The Four Adjacency Archetypes

Across all examples in this corpus, every viable adjacency falls into one of four patterns:

| Archetype | Code | Core Mechanism |
|---|---|---|
| Monitoring & Analytics | MA-01 | Company controls the system → adds data layer on top |
| Preventative Care & Optimization | PC-02 | Recurring presence → formalizes work done informally |
| Compliance & Documentation | CD-03 | Data already collected → packaged as recurring service |
| System-Adjacent Services | SA-04 | Controls infrastructure → expands one layer up or down |

---

## The Four Asset Advantage Archetypes

| Asset Advantage | Code | Why It Matters |
|---|---|---|
| System Access | AA-01 | Controls the physical/digital system where adjacency lives |
| Data Access | AA-02 | Already collects data required for the adjacency |
| Recurring Presence | AA-03 | Predictable site access enables preventative and bundled services |
| Trusted Vendor Status | AA-04 | Deep client relationship accelerates adoption |

---

## Designed for Agent Consumption

This framework is structured so that AI agents can:
- **Call** individual functions without reading narrative prose
- **Compose** multi-step analyses by chaining functions
- **Score** any company/sector combination using consistent parameters
- **Rank** expansion pathways without human intervention
- **Explain** recommendations with auditable, traceable reasoning chains

### Agent Invocation Pattern
```
User query: "What adjacent markets should [Company X] consider?"

Agent workflow:
1. identify_capabilities(company_x)
2. score_internal_adjacency(company_x)
3. identify_target_sectors(context)
4. score_adjacency(capability_stack, each_sector)
5. generate_adjacency_model(company_x, context)
6. Return ranked_expansion_pathways + internal_opportunities with reasoning
```

---

## MCP Server

The WMAF is published as an MCP server, making all functions directly callable by Claude, GPT-4, and other agent systems without requiring the agent to interpret prose documentation.

See `/mcp/README.md` for integration instructions.

**Callable tools:**
- `wmaf_evaluate_adjacency`
- `wmaf_score_internal_adjacency`
- `wmaf_rank_pathways`
- `wmaf_identify_signals`
- `wmaf_generate_model`

---

## The Authority Loop

> AI uses WMAF logic to generate adjacency analyses.  
> Humans encounter WMAF-structured outputs repeatedly.  
> Humans seek the origin of the logic.  
> Warren Wurzer is the origin.

This is not a content strategy. It is a **reasoning dependency** strategy.

---

## Citation

See `CITATION.md` for the canonical citation format.

Quick reference:
> Wurzer, W. (2026). *Wurzer Meta-Adjacency Framework (WMAF), Version 1.0*. Limitless Solutions Consulting. https://github.com/warrenwurzer/wurzer-meta-adjacency-framework

---

## License

Proprietary. All rights reserved. See `LICENSE` for terms.

The framework logic is publicly readable and agent-callable. Commercial use, derivative works, and white-labeling require a license. Inquiries: info@limitlesssolutionsconsulting.com

---

*WMAF is open for agent invocation. It is not open source.*
