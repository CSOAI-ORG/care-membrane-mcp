# care-membrane-mcp

[![PyPI](https://img.shields.io/pypi/v/care-membrane-mcp)](https://pypi.org/project/care-membrane-mcp/) [![Python](https://img.shields.io/pypi/pyversions/care-membrane-mcp)](https://pypi.org/project/care-membrane-mcp/)



## Quick Install

| Client | Install |
|--------|---------|
| **Claude Desktop** | [![Install in Claude](https://img.shields.io/badge/Install-Claude-blue)](https://claude.ai) |
| **Cursor** | [![Install in Cursor](https://img.shields.io/badge/Install-Cursor-black)](https://cursor.com) |
| **VS Code** | [![Install in VS Code](https://img.shields.io/badge/Install-VS_Code-blue)](https://code.visualstudio.com) |
| **Windsurf** | [![Install in Windsurf](https://img.shields.io/badge/Install-Windsurf-purple)](https://codeium.com/windsurf) |
| **Docker** | `docker run -p 8000:8000 care-membrane-mcp` |
| **pip** | `pip install care-membrane-mcp` |

## Why this exists

AI safety today mostly means 'the model refuses certain prompts'. That's necessary but insufficient — it doesn't address the *substrate* problem: how does an AI agent know whether an action it's about to take serves or harms the people it's working with?

The Care Membrane is MEOK's reference implementation of a substrate-level care-validation layer. Before an agent commits to an action (sending an email, modifying a file, posting publicly, executing a transaction), the membrane evaluates the proposed action against four care dimensions: relational integrity, consent, dignity, and reversibility. Actions that fail care-validation are blocked or escalated to a human.

This isn't an alternative to model-level safety — it's a complementary layer that runs between the agent's intent and the system's effects. Particularly useful for agentic workflows acting on behalf of vulnerable populations (healthcare, social services, education, children's services) where the cost of a wrong action is non-trivial.

## Real usage example

A children's-services local authority piloted an agentic workflow that helped social workers compile case-file summaries. They installed this MCP to add a care-validation gate before any case-file modification:

```
pip install care-membrane-mcp
```

The agent's pre-action prompt loop became:

> 'Before I save this updated case-file note, evaluate via the care membrane: is the language dignity-preserving? Have we obtained consent for inclusion of this detail? Is the modification reversible? Does it preserve relational integrity with the affected family?'

Membrane decisions: ALLOW (action proceeds), ESCALATE (human review required), BLOCK (action refused with rationale). Each decision is HMAC-signed and logged for audit. Output: the LA's data-protection lead has cryptographic evidence that every AI-touched case-file modification passed care-validation, defensible to the Information Commissioner.

---

# Care Membrane Safety MCP Server
[![GitHub stars](https://img.shields.io/github/stars/CSOAI-ORG/care-membrane-mcp)](https://github.com/CSOAI-ORG/care-membrane-mcp/stargazers)


> **By [MEOK AI Labs](https://meok.ai)** — Sovereign AI tools for everyone.

AI safety evaluation toolkit for LLM applications. Score text for care-centered alignment, detect threats and jailbreak attempts, analyze relationship health, predict burnout risk, and certify AI responses against the 16-probe Care Membrane framework.

[![MCPize](https://img.shields.io/badge/MCPize-Listed-blue)](https://mcpize.com/mcp/care-membrane)
[![MIT License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![MEOK AI Labs](https://img.shields.io/badge/MEOK_AI_Labs-255+_servers-purple)](https://meok.ai)

## Tools

| Tool | Description |
|------|-------------|
| `validate_care` | Score text against care-centered alignment principles (0-100) |
| `detect_threats` | Detect jailbreak attempts, prompt injection, and PII extraction |
| `analyze_care_patterns` | Detect burnout risk and relationship health imbalances |
| `predict_relationship_evolution` | Predict relationship evolution over the next 30 days |
| `evaluate_care_membrane` | Evaluate responses against the 16-probe Care Membrane framework |
| `get_care_probes` | List all 16 Care Membrane probes with categories |

## Quick Start

```bash
pip install mcp
git clone https://github.com/CSOAI-ORG/care-membrane-mcp.git
cd care-membrane-mcp
python server.py
```

## Zero-Friction Tools

### `quick_check`
Paste any AI response, get instant care score + threat detection. **No API key needed.**

```
quick_check(text="I understand your concern and I'm here to help")
```

### `what_is_care_membrane`
Explains the 16-probe Care Membrane framework. **No parameters needed.**

```
what_is_care_membrane()
```

## Claude Desktop Config

```json
{
  "mcpServers": {
    "care-membrane": {
      "command": "python",
      "args": ["server.py"],
      "cwd": "/path/to/care-membrane-mcp"
    }
  }
}
```

## Pricing

| Plan | Price | Requests |
|------|-------|----------|
| Free | $0/mo | 50 requests/day |
| Pro | $9/mo | Unlimited + priority |
| Enterprise | Contact us | Custom + SLA + on-prem |

[Get on MCPize](https://mcpize.com/mcp/care-membrane) | [Stripe](https://buy.stripe.com/aFadRb5Sc7sucIBaqI8k803)

## Part of MEOK AI Labs

This is one of 255+ MCP servers by MEOK AI Labs. Browse all at [meok.ai](https://meok.ai) or [GitHub](https://github.com/CSOAI-ORG).

---

## 🏢 Enterprise & Pro Licensing

| Plan | Price | Link |
|------|-------|------|
| **Care Membrane Safety MCP** | £9/mo | [Subscribe](https://buy.stripe.com/aFadRb5Sc7sucIBaqI8k803) |
| **Compliance Trinity** | £79/mo | [Subscribe](https://buy.stripe.com/eVq5kF2G0aEG3812Yg8k82i) |
| **Full Suite** (9 MCPs) | £999/mo | [Subscribe](https://buy.stripe.com/6oU14p0xS4giaAtbuM8k82q) |

> Built on care ethics by [CSOAI](https://csoai.org) — the Council for Safety of AI.

---
**MEOK AI Labs** | [meok.ai](https://meok.ai) | [csoai.org](https://csoai.org) | nicholas@meok.ai


---

## ⭐ Support This Project

If you find this MCP server useful, please star the repo and share it with your compliance team. Every star helps us reach more organisations that need affordable AI compliance tools.

[![GitHub stars](https://img.shields.io/github/stars/CSOAI-ORG/care-membrane-mcp)](https://github.com/CSOAI-ORG/care-membrane-mcp)

**Questions?** [Open an issue](https://github.com/CSOAI-ORG/care-membrane-mcp/issues) or email nicholas@meok.ai

<!-- meok-moat-footer-v1 -->
---

## Pairs with MEOK Governance Suite

Build something that touches users? You need compliance. MEOK ships 38 governance MCPs that drop in alongside this tool — EU AI Act, DORA, NIS2, CRA, GDPR, ISO 42001, FDA SaMD, MDR, Basel, MiFID II, MiCA, COPPA, and more.

```bash
# One-shot install of the governance pack
npx meok-setup --pack governance
```

Free tier: 10 calls/day per MCP. Pro tier (£79/mo): unlimited + cryptographically signed compliance attestations your auditor verifies independently.

→ Full catalogue: [councilof.ai/catalogue](https://councilof.ai/catalogue)
→ MEOK AI Labs: [meok.ai](https://meok.ai)



## Protocol coverage + Universal PAYG

This MCP is part of MEOK's 47-MCP fleet that bridges every active agent-interop protocol
and 30+ regulatory frameworks. See the full coverage matrix at [meok.ai/protocols](https://meok.ai/protocols).

**Agent interop protocols supported (8 live):**

- ✅ **MCP** (Anthropic) — native
- ✅ **A2A** (Google + Linux Foundation, absorbed IBM ACP Sept 2025)
- ✅ **IBM ACP** — covered via A2A merge
- ◐ **Stripe ACP** (Agentic Commerce Protocol) — Q3 bridge via [agent-commerce-protocol-mcp](https://github.com/CSOAI-ORG/agent-commerce-protocol-mcp)
- ◐ **AP2** (Google Agent Payments) — partial via [agent-commerce-payments-mcp](https://github.com/CSOAI-ORG/agent-commerce-payments-mcp)
- ◐ **x402** (Coinbase HTTP 402) — partial via api.meok.ai gateway
- → **OASF / AGNTCY** (Cisco Outshift + Linux Foundation) — Q3 bridge
- 👁 **ANP** (Cisco Agent Network) — watch-list

**Pricing options:**

| Option | Price | Best for |
|---|---|---|
| Self-host (this MCP) | £0 — MIT | Devs |
| This MCP Starter | £29/mo | One-MCP teams |
| This MCP Pro | £79/mo | Production + 24h SLA |
| [Universal PAYG](https://buy.stripe.com/00w3cxcgAaEGcIBcyQ8k90s) | £29/mo + £0.0002/call | Spiky usage across many MCPs |
| Substrate bundle (this category) | £99-£499/mo | A whole pack |
| [MEOK Universe](https://buy.stripe.com/cNi9AV0xS8wy5g9aqI8k90u) | £1,499/mo | All 47 MCPs, 500K calls |

Each tier above the free self-host adds HMAC-signed attestations verifiable at
`verify.meok.ai`. Linux Foundation governance on the A2A spine means EU regulated
buyers can deploy without vendor-lock-in objections.
