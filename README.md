<!-- BlackRoad SEO Enhanced -->

# agent skills

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad Agents](https://img.shields.io/badge/Org-BlackRoad-Agents-2979ff?style=for-the-badge)](https://github.com/BlackRoad-Agents)
[![License](https://img.shields.io/badge/License-Proprietary-f5a623?style=for-the-badge)](LICENSE)

**agent skills** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

## About BlackRoad OS

BlackRoad OS is a sovereign computing platform that runs AI locally on your own hardware. No cloud dependencies. No API keys. No surveillance. Built by [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc), a Delaware C-Corp founded in 2025.

### Key Features
- **Local AI** — Run LLMs on Raspberry Pi, Hailo-8, and commodity hardware
- **Mesh Networking** — WireGuard VPN, NATS pub/sub, peer-to-peer communication
- **Edge Computing** — 52 TOPS of AI acceleration across a Pi fleet
- **Self-Hosted Everything** — Git, DNS, storage, CI/CD, chat — all sovereign
- **Zero Cloud Dependencies** — Your data stays on your hardware

### The BlackRoad Ecosystem
| Organization | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform and applications |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate and enterprise |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | Artificial intelligence and ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware and IoT |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity and auditing |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing research |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | Autonomous AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh and distributed networking |
| [BlackRoad Education](https://github.com/BlackRoad-Education) | Learning and tutoring platforms |
| [BlackRoad Labs](https://github.com/BlackRoad-Labs) | Research and experiments |
| [BlackRoad Cloud](https://github.com/BlackRoad-Cloud) | Self-hosted cloud infrastructure |
| [BlackRoad Forge](https://github.com/BlackRoad-Forge) | Developer tools and utilities |

### Links
- **Website**: [blackroad.io](https://blackroad.io)
- **Documentation**: [docs.blackroad.io](https://docs.blackroad.io)
- **Chat**: [chat.blackroad.io](https://chat.blackroad.io)
- **Search**: [search.blackroad.io](https://search.blackroad.io)

---


50 AI skills across 6 modules for the BlackRoad OS agent fleet.

## What This Is

A structured registry of every skill available to BlackRoad agents. Skills are capabilities that any agent can invoke, organized by domain. The skill registry is used by the router and dispatch engine to match user requests to the right agent with the right capability.

## Modules

| Module | Count | Description |
|--------|-------|-------------|
| reasoning | 10 | Logic, causality, decision-making |
| code-generation | 10 | Python, JS, Bash, SQL, Rust, HTML/CSS |
| data-analysis | 8 | Logs, metrics, trends, capacity |
| creative | 8 | Writing, naming, summarization |
| system-ops | 7 | Health, deploy, DNS, backup, cron |
| security | 7 | Scanning, secrets, audit, hardening |

## Usage

```python
import json

with open("skills.json") as f:
    data = json.load(f)

# Find all skills in a module
code_skills = [s for s in data["skills"] if s["module"] == "code-generation"]

# Search skills by keyword
matches = [s for s in data["skills"] if "network" in s["description"].lower()]
```

```bash
# List all skill names
jq -r '.skills[].name' skills.json

# Count by module
jq -r '.skills | group_by(.module) | .[] | "\(.[0].module): \(length)"' skills.json
```

## Structure

Each skill object contains:

- `id` — Unique identifier (module prefix + number)
- `name` — Skill name (kebab-case)
- `module` — Parent module category
- `description` — What the skill does
- `example_prompt` — Example user input that would trigger this skill

Part of BlackRoad-Agents. Remember the Road. Pave Tomorrow. Incorporated 2025.
