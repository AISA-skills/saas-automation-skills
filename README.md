# SaaS Automation Skills

SaaS automation agent skills powered by AIsa.

This repository is part of the [AISA Skills](https://github.com/AISA-skills) collection. Each top-level directory is a self-contained agent skill with a `SKILL.md` file and optional supporting scripts, references, or assets.

## Skills

No active skills are currently published in this repository.

## Requirements

Most skills in this repository use AIsa APIs and expect one environment variable:

```bash
export AISA_API_KEY="your-aisa-api-key"
```

Get an API key at [aisa.one](https://aisa.one). Keep your key out of commits, screenshots, shared logs, and shell history exports.

## Install

Clone this repository:

```bash
git clone https://github.com/AISA-skills/saas-automation-skills.git
cd saas-automation-skills
```

Install one or more skills into your local agent runtime after skills are added. For Codex:

```bash
mkdir -p ~/.codex/skills
# cp -r <skill-name> ~/.codex/skills/
```

For other Agent Skills compatible runtimes, copy the skill folder into that runtime's skills directory, then restart the agent so it can load the skill metadata.

## Usage

Ask your agent to use the relevant skill by name. Example:

```text
Use <skill-name> to help me with this task.
```

Each skill contains its own workflow, safety rules, required inputs, and API notes in `SKILL.md`.

## Repository Layout

```text
saas-automation-skills/
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
