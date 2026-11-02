[Suomeksi](README.fi.md)

# agent-playbooks

Your AI agents build whatever you put in front of them. These packages add the roles that decide whether it was the right thing to build.

Agents, skills and playbooks for building products with AI agents in Claude Code, in English and Finnish. Each package is an installable Claude Code plugin with a guided setup, and every package can also be read on its own page here.

## Who it is for

People who build products with an agent team in Claude Code: founders, product owners and small teams who can now build almost anything and need help deciding what is worth building. No coding background is needed to use the packages; the setup asks you questions in plain language.

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

A package is usually built from these parts:

- **An agent** (`agents/`): a role with a fixed working method and a fixed answer format. It reads your project and recommends; you decide.
- **A setup skill** (`skills/setup/`): a step-by-step guide that Claude runs in your project. It stops for your approval after every step and tailors the agent to your project. The parts to tailor are marked `[FILL IN: ...]`.
- **Docs and examples** (`docs/`, `examples/`): the templates, the background research and a filled sample, so you can see the result before you start. Finnish translations are in `docs/fi/`.

A package can also be only a skill or a playbook without an agent. The packages work in any Claude Code project. They need no other system and no external service.

## Roadmap

- **Planned:** more of the roles, skills and playbooks from an agentic product team (for example a systems analyst, a QA role and the routines that connect them), published one package at a time. Each new package gets its own folder and its own page, and installs the same way.

## Review before use

These are prompts and instructions, not audited software. They are provided as is. Read the agent and skill files before you use them, and check what they write into your project.

## Licence

[MIT](LICENSE). Copyright (c) 2026 Simo Parviainen.

## Author

Created by Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
