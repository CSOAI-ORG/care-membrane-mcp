# Care Membrane Safety MCP Server

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
**MEOK AI Labs** | [meok.ai](https://meok.ai) | nicholas@meok.ai | United Kingdom
