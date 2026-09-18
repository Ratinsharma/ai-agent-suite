# AI Agent Suite

Seven Hermes-ready agent skills for sales, growth, partnerships, app building, automation, research, and graph reasoning.

Each agent is a self-contained Markdown playbook (`SKILL.md`) plus reusable templates. No application runtime lives in this repo — drop skills into a Hermes (or compatible) agent skill folder and invoke by mandate.

## Features

- **deal-closer** — sales execution manual (pipeline math, scripts, MEDDPICC, battle cards)
- **growth-engine** — marketing playbooks (unit economics, content calendar, email sequences)
- **partnership-builder** — alliance / partner scorecards and deal structures
- **app-forge** — web app scaffolding patterns (Theo stack, RAG, deploy checklists)
- **automation-architect** — SRE-style reliability, health checks, incident response
- **research-synthesizer** — paper/lab tracking and synthesis frameworks
- **graph-thinker** — knowledge graphs, Graph RAG, event-sourced non-loop architectures

## Stack

- Markdown `SKILL.md` agent playbooks (Hermes-oriented)
- Per-agent `templates/` for scorecards, checklists, and digests
- No runtime code

## Quickstart

1. Clone the repo:
   ```bash
   git clone https://github.com/Ratinsharma/ai-agent-suite.git
   cd ai-agent-suite
   ```
2. Copy the agent folder you need into your Hermes skills directory (or point Hermes at this repo).
3. Open that agent's `SKILL.md` and follow **WHEN TO USE** + frameworks.
4. Use files under `templates/` as working docs.

## Structure

```
ai-agent-suite/
├── deal-closer/              # sales playbook + templates
├── growth-engine/            # marketing playbook + templates
├── partnership-builder/      # partnerships playbook + templates
├── app-forge/                # app builder playbook + templates
├── automation-architect/     # reliability playbook + templates
├── research-synthesizer/     # research playbook + templates
├── graph-thinker/            # graph reasoning playbook + templates
├── LICENSE
├── CONTRIBUTING.md
└── README.md
```

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md). Prefer improving playbook accuracy and templates over drive-by rewrites.

## License

MIT — see [`LICENSE`](LICENSE).

## Author

Ratin Sharma