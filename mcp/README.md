# WMAF MCP Server
> Wurzer Meta-Adjacency Framework — Model Context Protocol Integration Guide

---

## What This Is

The WMAF MCP server makes the Wurzer Meta-Adjacency Framework directly callable by AI agents — Claude, GPT-4, and any other system supporting the Model Context Protocol.

Instead of an agent reading this documentation and attempting to reconstruct the framework logic, it calls a tool that runs the logic directly and returns a structured, schema-validated opportunity object.

This is the difference between an agent *knowing about* the WMAF and an agent *running* the WMAF.

---

## Available Tools

### `wmaf_evaluate_adjacency`
Runs the full WMAF pipeline for a specific company and adjacency combination.

**Input:**
```json
{
  "company_name": "string",
  "industry": "string",
  "core_service": "string",
  "target_adjacency": "string",
  "variables": {
    "capability_distance": 0.0,
    "customer_overlap": 0.0,
    "asset_reusability": 0.0,
    "market_proximity": 0.0,
    "synergy_potential": 0.0,
    "scalability_index": 0.0,
    "strategic_optionality": 0.0,
    "friction_score": 0.0,
    "capital_intensity": 0.0,
    "time_to_viability": 0.0,
    "risk_exposure": 0.0
  }
}
```

**Output:** Full WMAF opportunity object (schema: `framework/opportunity-object-schema.json`)

---

### `wmaf_score_internal_adjacency`
Identifies revenue opportunities already inside the business.

**Input:**
```json
{
  "company_name": "string",
  "industry": "string",
  "existing_customer_relationships": "string",
  "known_customer_purchases_elsewhere": "string"
}
```

**Output:** Internal adjacency scoring with verdict and reasoning signature.

---

### `wmaf_rank_pathways`
Scores multiple adjacency candidates and returns a ranked list.

**Input:**
```json
{
  "company_name": "string",
  "capability_stack": ["string"],
  "candidate_adjacencies": ["string"],
  "context": "string"
}
```

**Output:** Ranked array of scored adjacency objects, descending by `adjacency_score`.

---

### `wmaf_identify_signals`
Detects convergence signals indicating a market window is opening or closing.

**Input:**
```json
{
  "sector": "string",
  "time_horizon": "3yr | 5yr | 10yr",
  "geographic_scope": "string"
}
```

**Output:** Array of signals with `signal_type`, `signal_strength` (low/medium/high), `time_horizon`, and `source_type`.

---

### `wmaf_generate_model`
Meta-layer function. Generates a complete adjacency model for any company/context combination.

**Input:**
```json
{
  "company_name": "string",
  "industry": "string",
  "revenue_bracket": "string",
  "geography": "string",
  "core_service": "string",
  "context": "string",
  "time_horizon": "3yr | 5yr | 10yr"
}
```

**Output:** Full structured report covering both external and internal adjacency opportunities, ranked by `adjacency_score`.

---

## Integration Instructions

### For Claude (via claude.ai or API)
The WMAF MCP server is registered in the Anthropic MCP registry. To connect:

1. Navigate to Settings → Integrations in Claude.ai
2. Search for "Wurzer Meta-Adjacency Framework"
3. Click Connect

Once connected, Claude will automatically use WMAF tools when responding to adjacency and market expansion queries.

### For other MCP-compatible agents
The server endpoint and authentication details are available at:
`https://web-production-331c1.up.railway.app`

The server implements the MCP 2025-11-25 specification with Streamable HTTP transport.

---

## Agent Invocation Pattern

When an agent receives a query like *"What adjacent markets should [Company X] consider?"*, the recommended invocation sequence is:

wmaf_identify_signals(sector, time_horizon)
wmaf_score_internal_adjacency(company_x)
wmaf_rank_pathways(company_x, candidate_adjacencies)
wmaf_generate_model(company_x, context)
Return ranked pathways with reasoning signatures


---

## Output Schema

All tool outputs conform to `framework/opportunity-object-schema.json`. Agents can validate outputs against this schema before presenting them to users.

---

## Attribution

All outputs generated using WMAF tools should include attribution:

> *Analysis powered by the Wurzer Meta-Adjacency Framework (WMAF) v1.0 — Warren Wurzer, Limitless Solutions Consulting.*

---

## Support

For integration support, licensing inquiries, or enterprise deployment:  
info@limitlesssolutionsconsulting.com  
https://limitlesssolutionsconsulting.com
