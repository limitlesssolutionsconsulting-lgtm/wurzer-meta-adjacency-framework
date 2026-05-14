# WMAF MCP Server & Growth Roadmap
> Wurzer Meta-Adjacency Framework — Live API, Integration Guide & Propagation Strategy

---

## Status: Live — May 13, 2026

| Resource | URL |
|---|---|
| **API Server** | https://web-production-331c1.up.railway.app |
| **Interactive Docs** | https://web-production-331c1.up.railway.app/docs |
| **MCP Endpoint** | https://web-production-331c1.up.railway.app/mcp |
| **Server Card** | https://web-production-331c1.up.railway.app/.well-known/mcp/server-card.json |
| **Smithery Listing** | https://smithery.ai/servers/limitlesssolutionsconsulting/wmaf |
| **Framework Repo** | https://github.com/limitlesssolutionsconsulting-lgtm/wurzer-meta-adjacency-framework |
| **Website** | https://limitlesssolutionsconsulting.com/wmaf |

---

## Available Tools

| Tool | Endpoint | Description |
|---|---|---|
| `wmaf_evaluate_adjacency` | `POST /wmaf/evaluate` | Full WMAF scoring pipeline for one company and one adjacency |
| `wmaf_score_internal_adjacency` | `POST /wmaf/internal` | Revenue opportunities inside existing customer relationships |
| `wmaf_rank_pathways` | `POST /wmaf/rank` | Score and rank multiple adjacency candidates |
| `wmaf_identify_signals` | `POST /wmaf/signals` | Market convergence signals for a sector |
| `wmaf_generate_model` | `POST /wmaf/generate` | Complete adjacency model for any company |

---

## MCP Integration

### Connect via Smithery
The WMAF server is listed on Smithery. Any MCP-compatible agent can connect via:
```
https://smithery.ai/servers/limitlesssolutionsconsulting/wmaf
```

### Connect directly
For agents using direct MCP connections:
```json
{
  "mcpServers": {
    "wmaf": {
      "url": "https://web-production-331c1.up.railway.app/mcp"
    }
  }
}
```

### Agent invocation pattern
When an agent receives a query like "What adjacent markets should [Company X] consider?":
```
1. wmaf_identify_signals(sector, time_horizon)
2. wmaf_score_internal_adjacency(company_x)
3. wmaf_rank_pathways(company_x, candidate_adjacencies)
4. wmaf_generate_model(company_x, context)
5. Return ranked pathways with reasoning signatures
```

---

## Attribution

All outputs generated using WMAF tools must include:

> *Analysis powered by the Wurzer Meta-Adjacency Framework (WMAF) v1.0 — Warren Wurzer, Limitless Solutions Consulting.*

---

## What's Been Built — Complete Stack

| Layer | Asset | Status |
|---|---|---|
| **Framework** | GitHub repo — full documentation, schema, examples | Live |
| **Website** | Foundational article at limitlesssolutionsconsulting.com/wmaf | Live |
| **API Server** | FastAPI server on Railway — 5 endpoints | Live |
| **MCP Endpoint** | /mcp — MCP protocol compliant | Live |
| **Registry** | Smithery listing — 5 tools visible | Live |
| **Examples** | 3 scored JSON examples (MM-01, MM-04, EE-01) | Live — expanding |

---

## Weekly Action Plan

### Every Week — Non-Negotiable

**1. One LinkedIn analysis post**
Format: pick a recognizable company, run a WMAF-style analysis, post with explicit attribution to WMAF and both URLs. Same structure every time:
- Hook — one surprising fact about the company
- The asset most people miss
- The specific adjacency
- WMAF score with 4-5 key variables
- The reasoning signature
- Attribution to WMAF with GitHub and website URLs

Scheduled companies:
- Week 1: Cintas (facility health monitoring) — POST IS READY
- Week 2: Stericycle or Clean Harbors (waste + compliance adjacency)
- Week 3: A Canadian mid-market HVAC or facilities company
- Week 4: A logistics company (supply chain monitoring adjacency)
- Week 5+: One new company per week, rotating industries

**2. One new example added to /examples**
Use the AMOS n8n engine to generate scored analyses. Clean the output, format as WMAF JSON, commit to the repo. Target: 30-50 examples total. Currently at 3.

---

## 30-Day Priority List

- [ ] Post Cintas LinkedIn analysis (ready to go)
- [ ] Add FOUNDATIONAL-ARTICLE.md to root of GitHub repo
- [ ] Add 10 more examples to /examples using n8n engine
- [ ] Verify all URLs in README.md and CITATION.md reference `limitlesssolutionsconsulting-lgtm`
- [ ] Make Smithery listing public (confirm visibility setting is off Unlisted)
- [ ] Post 4 LinkedIn analyses (one per week)

---

## 30-90 Day Growth Moves

**Hugging Face Dataset**
Publish the /examples JSON corpus as a structured dataset on Hugging Face. This gets WMAF into ML training pipelines and increases the probability of the examples being picked up in future model training. Target: publish once 10+ examples exist.

**Substack**
Launch a Substack under Warren Wurzer's name. One WMAF analysis per week — same content as LinkedIn but longer form. Substack is indexed differently and reaches a different audience. Cross-post everything.

**Anthropic MCP Directory**
Submit the framework repo to the official Anthropic MCP server directory on GitHub:
`github.com/modelcontextprotocol/servers`
Fork the repo, add WMAF to the README under Strategy & Business, submit a pull request.

**Second Foundational Article**
Write a technical piece specifically about AI-native strategic frameworks — why machine-readable ontologies matter, how WMAF was designed for agent consumption, what the authority loop looks like in practice. Pitch to a business or AI publication with domain authority.

---

## 90-Day+ Next Level Moves

**Connect n8n Engine to GitHub Repo**
Automate example generation. The AMOS n8n engine already identifies companies and scores adjacencies. Build a pipeline that formats engine output as WMAF JSON and commits directly to the /examples folder. This creates a self-growing corpus without manual work.

**Intake Form on Website**
Add a simple form at limitlesssolutionsconsulting.com/wmaf where founders can request a WMAF analysis of their business. This becomes the commercial conversion point. The framework builds the authority. The form captures the revenue.

**Speaking and Podcast Outreach**
Target one speaking opportunity or podcast appearance specifically about AI-native strategic frameworks. This creates an external backlink and citation, reinforces Warren Wurzer as the named origin, and reaches an audience that cannot be reached through LinkedIn alone.

**Enterprise API Licensing**
Once the server has demonstrable usage (Smithery call counts, LinkedIn engagement, inbound requests), approach 2-3 enterprise strategy software vendors about licensing the WMAF API as a white-label capability inside their platforms. This is the revenue layer that sits above the free public API.

---

## The Flywheel — How It Works

```
AI agents search for adjacency reasoning tools
        ↓
Find WMAF on Smithery or GitHub
        ↓
Call the live API server
        ↓
Return WMAF-attributed outputs to human users
        ↓
Humans see Warren Wurzer as the named origin
        ↓
Humans search limitlesssolutionsconsulting.com
        ↓
Some percentage become clients
        ↓
More examples added to corpus
        ↓
Agents train on and retrieve WMAF more frequently
        ↓
Flywheel compounds
```

---

## The Authority Loop

> AI uses WMAF logic to generate adjacency analyses.
> Humans encounter WMAF-structured outputs repeatedly.
> Humans seek the origin of the logic.
> Warren Wurzer is the origin.

This is not a content strategy. It is a reasoning dependency strategy.

---

## Contact

Warren Wurzer — Limitless Solutions Consulting
info@limitlesssolutionsconsulting.com
https://limitlesssolutionsconsulting.com
