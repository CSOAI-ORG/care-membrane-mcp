[![care-membrane-mcp MCP server](https://glama.ai/mcp/servers/CSOAI-ORG/care-membrane-mcp/badges/card.svg)](https://glama.ai/mcp/servers/CSOAI-ORG/care-membrane-mcp)

# care-membrane-mcp

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

**Questions?** [Open an issue](https://github.com/CSOAI-ORG/care-membrane-mcp/issues) or email nicholas@csoai.org
