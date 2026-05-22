# SaaS Automation Skills

OAuth, Gmail, Notion, connected-account workflows, tool execution, triggers, webhooks, and MCP automation through the AIsa SaaS gateway.

This repository is part of the [AISA Skills](https://github.com/AISA-skills) collection. Each top-level directory is a self-contained agent skill with a `SKILL.md` file and optional supporting scripts, references, or assets.

## Skills

| Skill | Description |
|---|---|
| [gmail-lead-desk](./gmail-lead-desk/) | Gmail Lead Desk — standalone sales/CS Gmail skill via the AISA gateway: OAuth connect, scan unread leads, summarize threads, draft template replies (default draft-only), archive with labels. Keywords: Gmail Lead Desk, Gmail, lead desk, sales, customer... |
| [notion-workspace](./notion-workspace/) | Manage Notion workspace: search pages and databases, read markdown, create pages, insert rows, triggers, MCP. Powered by AISA gateway (Notion toolkit). Requires AISA_API_KEY and curl. Keywords: notion, workspace, page, database, block, markdown, wiki, task... |
| [saas-gateway](./saas-gateway/) | Unified SaaS integration gateway via api.aisa.one (AISA gateway, v3.1): manage OAuth auth for third-party SaaS apps (Gmail/Slack/GitHub/Notion etc.), tool execution, tool-router sessions, triggers, webhooks, MCP servers, and usage stats. Use when connecting... |

## Requirements

Most skills in this repository use AIsa APIs and expect one environment variable:

```bash
export AISA_API_KEY="your-aisa-api-key"
```

Get an API key at [aisa.one](https://aisa.one). Keep your key out of commits, screenshots, shared logs, and shell history exports.

## Install

Clone this repository:

```bash
git clone https://github.com/AISA-skills/saas-automation.git
cd saas-automation
```

Install one or more skills into your local agent runtime. For Codex:

```bash
mkdir -p ~/.codex/skills
cp -r gmail-lead-desk ~/.codex/skills/
cp -r notion-workspace ~/.codex/skills/
cp -r saas-gateway ~/.codex/skills/
```

For other Agent Skills compatible runtimes, copy the skill folder into that runtime's skills directory, then restart the agent so it can load the skill metadata.

## Usage

Ask your agent to use the relevant skill by name. Example:

```text
Use gmail-lead-desk to help me with this task.
```

Each skill contains its own workflow, safety rules, required inputs, and API notes in `SKILL.md`.

## Repository Layout

```text
saas-automation/
|-- README.md
|-- LICENSE
|-- .gitignore
`-- <skill-name>/
    |-- SKILL.md
    |-- scripts/       # optional
    |-- references/    # optional
    `-- assets/        # optional
```

## Contributing

1. Keep each skill self-contained in its own folder.
2. Keep `SKILL.md` focused on agent-facing instructions.
3. Put large endpoint docs, schemas, templates, or examples in `references/`.
4. Put deterministic helper code in `scripts/`.
5. Do not commit local outputs, credentials, caches, or API responses.

## License

MIT. See [LICENSE](./LICENSE).
