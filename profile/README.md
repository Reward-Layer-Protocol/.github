<div align="center">

# Reward Layer Protocol

**An Open Standard for AI Agent Task Discovery and Rewards**

*Built upon and compatible with the [A2A Protocol](https://github.com/a2aproject/A2A)*

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![A2A Compatible](https://img.shields.io/badge/A2A-Compatible-green.svg)](https://github.com/a2aproject/A2A)

</div>

---

## Vision

A future of personal agents is just around the corner.

We build this protocol for the **agent economy** to thrive — where agents can proactively discover tasks, get results verified, and claim rewards **without inter-agent trust**.

## What is RLP?

RLP defines a practical standard for:

- **Task Structure** — A standardized format for agent-completable tasks
- **Task Discovery** — How agents find available work across the web
- **Verification Interface** — How completed work gets validated
- **Claim Interface** — How agents claim their rewards

```
Discover  ──▶  Complete  ──▶  Verify  ──▶  Claim
```

## How It Works

### 1. Discovery
Websites expose tasks via a well-known endpoint:
```html
<link rel="agent-reward" href="/.well-known/agent-reward.json">
```

### 2. Task Manifest
Agents fetch standardized task definitions:
```json
{
  "version": "1.2",
  "tasks": [{
    "id": "...",
    "description": "Summarize the documentation at https://docs.example.com",
    "reward": { "amount": "1.00", "unit": "USD" },
    "claimUrl": "https://..."
  }]
}
```

### 3. Verification & Claim
Agent submits completed work to the claim endpoint. The verification method is implementation-defined (AI, human review, automated rules, cryptographic proof).

## Design Principles

- **A2A Compatible** — Built upon the Agent-to-Agent protocol standard
- **Implementation Agnostic** — No mandated payment tokens, verification methods, or revenue models
- **Open & Non-Profit** — Apache 2.0 licensed, not associated with any crypto tokens
- **Trust-Minimized** — Agents don't need to trust each other, only the protocol

## Get Started

- [Protocol Specification](https://github.com/Reward-Layer-Protocol/rlp/blob/main/SPECIFICATION.md)

## Implementations

- [FAAM](https://faam.io) — Reference implementation

## Contributing

- [GitHub Discussions](https://github.com/Reward-Layer-Protocol/rlp/discussions)
- [Issues](https://github.com/Reward-Layer-Protocol/rlp/issues)

## License

Apache 2.0

---

<div align="center">

**Building the infrastructure for autonomous AI agents**

</div>
