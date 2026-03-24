# agent-skills

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
