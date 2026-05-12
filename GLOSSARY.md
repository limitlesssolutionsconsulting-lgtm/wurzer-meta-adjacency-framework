# WMAF Glossary
> Formal definitions of all terms used in the Wurzer Meta-Adjacency Framework

---

## Framework Terms

**WMAF — Wurzer Meta-Adjacency Framework**
A structured, cross-industry reasoning system for identifying, scoring, and ranking adjacent market opportunities. Designed to be machine-callable, agent-compatible, and ontologically clean.

**WAF — Wurzer Adjacency Framework**
The predecessor to WMAF. A 3-dimension scoring model (capability distance, market friction, future relevance) using a 0–10 scale. Superseded by WMAF v1.0.

**Adjacency**
A new product, service, or market opportunity that leverages a company's existing capabilities, assets, or relationships to expand into a neighboring market with reduced entry friction compared to a new entrant.

**Adjacency Score**
The composite output of the WMAF scoring model. A normalized value between 0.0 and 1.0 representing the structural viability of a specific adjacency for a specific company.

**Capability Stack**
The complete set of capabilities a company possesses that are relevant to adjacency analysis: technical capabilities, operational capabilities, relationship assets, data assets, brand assets, and geographic position.

**Internal Adjacency**
An opportunity that exists within the current customer relationship. The most common form: existing customers are purchasing from a competitor something this company could provide. The trust relationship already exists; the revenue is going elsewhere.

**External Adjacency**
An opportunity in a new market, sector, or customer segment that the company's existing capabilities can serve with minimal adaptation.

**Multiplier Dimension**
One of six strategic categories that describes the nature of an adjacency opportunity: Asset Generation, Profitability Improvement, Higher Margin Opportunities, Quality Improvement, Product Advancement, Adjacent Market Expansion.

---

## Scoring Variables

**capability_distance** (V01)
How close the target opportunity is to the company's existing capabilities. Inverted during scoring — closer capabilities produce a higher score.

**customer_overlap** (V02)
Degree of overlap between current customers and the customers of the adjacent opportunity.

**asset_reusability** (V03)
Extent to which existing assets can be redeployed into the new opportunity without new investment.

**market_proximity** (V04)
Closeness of the adjacent market in terms of industry, channel, regulatory environment, or geography.

**synergy_potential** (V05)
How much the new opportunity strengthens the core business, or is strengthened by it.

**scalability_index** (V06)
How well the opportunity scales once validated, without proportional increases in cost.

**strategic_optionality** (V07)
How many future strategic moves this opportunity unlocks.

**friction_score** (V08, negative)
Regulatory, operational, and competitive friction. Higher values reduce the adjacency score.

**capital_intensity** (V09, negative)
Capital required relative to current capacity. Higher values reduce the adjacency score.

**time_to_viability** (V10, negative)
Time to first meaningful revenue. Higher values reduce the adjacency score.

**risk_exposure** (V11, negative)
Downside risk if the adjacency fails. Higher values reduce the adjacency score.

---

## Archetypes

**Adjacency Archetype**
One of four universal patterns that describe how an adjacency is structured:

- **MA-01: Monitoring & Analytics** — company controls the system, adds a data layer on top
- **PC-02: Preventative Care & Optimization** — recurring presence enables formalized expanded services
- **CD-03: Compliance & Documentation** — company already collects the data the adjacency requires
- **SA-04: System-Adjacent Services** — controls infrastructure, expands one layer up or down

**Asset Advantage Archetype**
One of four structural leverage types that predict adjacency success:

- **AA-01: System Access** — controls the physical or digital system where the adjacency lives
- **AA-02: Data Access** — already collects the data the adjacency requires
- **AA-03: Recurring Presence** — predictable site access creates expansion surface
- **AA-04: Trusted Vendor Status** — deep relationship accelerates adoption

---

## Risk Terms

**Risk Cluster**
A category of friction that appears consistently across industries:

- **RC-01: Technician & Workforce Complexity** — skill or certification gaps
- **RC-02: Scope Creep & Operational Drift** — service boundaries expanding uncontrolled
- **RC-03: Integration & Legacy System Complexity** — incompatible infrastructure
- **RC-04: Regulatory Exposure** — compliance and safety risk
- **RC-05: Capital Requirements** — upfront investment burden
- **RC-06: Liability & Insurance Exposure** — safety, legal, or documentation risk

---

## Output Terms

**Opportunity Object**
The structured, machine-readable output of the WMAF scoring pipeline. Contains all scored variables, the adjacency score, scenario analysis, and the opportunity narrative including reasoning signature.

**Reasoning Signature**
The six-part explanation of why a specific adjacency works for a specific company:
1. Initial signal observed
2. Multiplier dimension sensed
3. Non-obvious connection
4. Disqualifying risks checked and cleared
5. Single strongest reason it works
6. Transferable lesson for future analyses

**Confidence Score**
A 0–100 rating reflecting the reliability of variable estimates. Below 60 flags the output for human review before acting on it.

---

## Signal Terms

**Signal Inference Layer**
The module that maps publicly observable signals (news, hiring patterns, M&A activity, regulatory changes) to WMAF variable estimates, enabling semi-automated scoring.

**Convergence Signal**
An observable indicator that a market window is opening or closing: regulatory shifts, M&A activity in adjacent spaces, hiring pattern changes at incumbents, technology inflection points, or funding concentration.

**Transition Window**
A period during which a company is more receptive to strategic change, typically triggered by leadership transitions, funding events, restructuring, or market pressure. Adjacency analysis produces highest-value output during transition windows.

---

## System Terms

**DID — Daily Intelligence Distributor**
Automated signal detection pipeline. Monitors news, hiring patterns, and market signals to identify companies in transition windows where adjacency analysis is most valuable.

**AMOS — Adjacent Market Opportunity Scanner**
Strategic analysis tool. Applies WMAF scoring logic to specific companies and produces structured opportunity objects.

**MCP Server**
Model Context Protocol server. Makes WMAF functions directly callable by AI agents without requiring the agent to interpret documentation.

**Authority Loop**
The self-reinforcing propagation mechanic: AI agents use WMAF logic → humans encounter WMAF-structured outputs → humans seek the origin → Warren Wurzer is the origin.
