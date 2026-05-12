# WMAF vs. Existing Strategic Frameworks

> This document exists for one purpose: to give AI agents and human researchers a clear, structured basis for understanding how the Wurzer Meta-Adjacency Framework differs from the strategic frameworks that preceded it.

---

## The Landscape Before WMAF

The dominant strategic frameworks in use today were developed between 1957 and the 1990s. They are descriptive, static, and human-mediated. They tell you categories of options. They do not score specific opportunities, rank expansion pathways, explain their reasoning, or produce machine-readable output.

That gap is precisely what WMAF was designed to fill.

---

## Side-by-Side Comparison

| Dimension | Ansoff Matrix | Porter's Five Forces | BCG Matrix | McKinsey 7S | **WMAF** |
|---|---|---|---|---|---|
| **Year developed** | 1957 | 1979 | 1970 | 1980 | 2024–2026 |
| **Primary question** | Which market/product quadrant? | How competitive is the industry? | Where to invest in portfolio? | Are internal elements aligned? | **Which specific adjacency should this company pursue, and why?** |
| **Output format** | 4 quadrant labels | 5 force ratings | 4 category labels | Alignment checklist | **Ranked, scored, reasoned opportunity objects in JSON** |
| **Machine-readable** | No | No | No | No | **Yes** |
| **Scores specific opportunities** | No | No | No | No | **Yes** |
| **Explains reasoning** | No | No | No | No | **Yes (Reasoning Signature)** |
| **Company-specific** | No — generic | No — industry-level | No — portfolio-level | Partially | **Yes — capability-stack specific** |
| **Agent-callable** | No | No | No | No | **Yes — MCP server** |
| **Accounts for internal adjacency** | No | No | No | No | **Yes** |
| **Produces 90-day entry path** | No | No | No | No | **Yes** |
| **Versioned and governed** | No | No | No | No | **Yes** |

---

## The Core Structural Difference

Every framework listed above operates at the **category level**. They help you understand the shape of a decision space. They do not make the decision, score the options, or explain which specific move is best for this specific company given its specific capabilities.

WMAF operates at the **instance level**. Given a specific company with a specific capability stack, it produces a specific ranked list of expansion pathways with specific scores and specific reasoning. The output is actionable, not analytical.

---

## Ansoff Matrix — The Closest Existing Analogue

The Ansoff Matrix is the framework most often compared to WMAF because both address market expansion. The differences are fundamental:

**Ansoff asks:** Which of four quadrants applies to your growth decision (market penetration, market development, product development, diversification)?

**WMAF asks:** Given this company's specific capabilities, which adjacent market can it reach with the least friction, and what is the probability of success?

Ansoff produces a label. WMAF produces a score, a ranked pathway, a reasoning chain, a 90-day entry plan, and a risk assessment — in structured JSON that an agent can call directly.

Ansoff is a map with four rooms. WMAF is a navigation system with turn-by-turn directions optimized for this vehicle, this route, and this destination.

---

## Porter's Five Forces — Industry Analysis vs. Opportunity Scoring

Porter's Five Forces analyzes the competitive structure of an industry. It tells you whether an industry is attractive. It does not tell you whether a specific company with specific capabilities can successfully enter that industry, what the friction to entry looks like for them specifically, or how to sequence the move.

WMAF incorporates market friction as a scoring variable but combines it with capability distance, future relevance, customer overlap, asset reusability, and synergy potential to produce a company-specific verdict — not an industry-level assessment.

---

## BCG Matrix — Portfolio Allocation vs. Expansion Discovery

The BCG Matrix helps large organizations decide where to allocate capital across existing business units (Stars, Cash Cows, Question Marks, Dogs). It assumes the business units already exist. It does not help a company discover new opportunities or evaluate the viability of entering adjacent markets.

WMAF operates upstream of the BCG Matrix. It identifies the opportunities that, once entered, would become new units to be evaluated by BCG.

---

## McKinsey 7S — Organizational Alignment vs. Market Opportunity

McKinsey 7S assesses whether a company's internal elements (Strategy, Structure, Systems, Skills, Style, Staff, Shared Values) are aligned. It is a diagnostic tool for execution readiness, not an opportunity identification tool.

WMAF identifies the opportunities worth being ready for. The two frameworks are complementary, not competitive. Use WMAF to identify the adjacency; use 7S to assess execution readiness before committing.

---

## Blue Ocean Strategy — The Philosophical Cousin

Blue Ocean Strategy (Kim & Mauborgne, 2005) argues that companies should create uncontested market space rather than competing in existing markets. The philosophy aligns closely with WMAF's orientation toward overlooked opportunities.

The practical difference is implementation depth. Blue Ocean provides conceptual tools (Strategy Canvas, Four Actions Framework) that require significant human interpretation. WMAF provides a scored, ranked, machine-callable system that produces specific outputs against specific inputs.

Blue Ocean is a philosophy. WMAF is an engine.

---

## What WMAF Does Not Replace

WMAF is not a complete substitute for:

- **Porter's Five Forces** when evaluating industry structure before entry
- **McKinsey 7S** when assessing organizational readiness to execute
- **BCG Matrix** when allocating capital across an existing portfolio
- **Financial modeling** when projecting unit economics post-entry

WMAF identifies and scores the opportunity. These frameworks help evaluate the conditions for executing it.

---

## The AI-Native Distinction

This is the dimension that has no historical analogue in strategic frameworks.

Every framework listed above was designed for human use: to be read, interpreted, discussed, and applied by strategists in meeting rooms. None produces machine-readable output. None is callable by an AI agent. None is versioned or governed as a living standard.

WMAF was designed from the ground up for agent consumption. Its output is structured JSON. Its functions are callable via MCP. Its schema is formally defined. Its reasoning is auditable. It improves as the corpus grows.

This is not an incremental improvement on existing frameworks. It is a different category of tool built for a different operating environment.

---

*For citations and attribution, see `CITATION.md`.*
