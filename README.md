[Suomeksi](README.fi.md)

# agent-playbooks

Your AI agents build whatever you put in front of them. These packages add the roles that decide whether it was the right thing to build.

Claude Code agents and playbooks for building products with an agent team, in English and Finnish. Each package is an installable Claude Code plugin with a guided setup.

## Install

In Claude Code, run:

```
/plugin marketplace add Simopee/agent-playbooks
/plugin install head-of-product@simopee-agent-playbooks
```

Then start the setup with `/head-of-product:setup`.

**No install:** paste the link `https://github.com/Simopee/agent-playbooks` into Claude Code in your project and ask whether it would help your project. Claude can read the files and walk you through the setup without installing anything.

## What's inside

| Package | What it does | Docs |
|---|---|---|
| [head-of-product](plugins/head-of-product/) | A Head of Product agent that judges your product work against a written strategy, plus a guided setup that writes that strategy with you. | [English](plugins/head-of-product/README.md), [suomeksi](plugins/head-of-product/README.fi.md) |

## How it works

Each package has three parts:

- **An agent** (`agents/`): a role with a fixed working method and a fixed answer format. It reads your project and recommends; you decide.
- **A setup skill** (`skills/setup/`): a step-by-step guide that Claude runs in your project. It stops for your approval after every step and tailors the agent to your project. The parts to tailor are marked `[FILL IN: ...]`.
- **Docs and examples** (`docs/`, `examples/`): the templates, the background research and a filled sample, so you can see the result before you start. Finnish translations are in `docs/fi/`.

The packages work in any Claude Code project. They need no other system and no external service.

## Roadmap

- **Planned:** more agents from an agentic product team, published one at a time.

## Review before use

These are prompts and instructions, not audited software. They are provided as is. Read the agent and skill files before you use them, and check what they write into your project.

## Licence

[MIT](LICENSE). Copyright (c) 2026 Simo Parviainen.

## Author

Created by Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
