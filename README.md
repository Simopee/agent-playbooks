[Suomeksi](README.fi.md)

# agent-playbooks

Your AI agents will build whatever you put in front of them. These packages add roles that help you decide whether it is worth building.

This repo holds agents, skills and playbooks for building products with AI agents in Claude Code, in English and Finnish. Each package installs as a Claude Code plugin with a guided setup. You can also read each package on its own page here.

## Who it is for

Founders, product owners and small teams who build products with a team of agents in Claude Code. Your agents can now build almost anything, so the hard part is deciding what is worth building. You do not need to know how to code: the setup asks you questions in plain language.

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

A package usually has these parts:

- **An agent** (`agents/`): a role with a fixed working method and a fixed answer format. It reads your project and recommends; you decide.
- **A setup skill** (`skills/setup/`): a step-by-step guide that Claude runs in your project. It tailors the agent to your project and stops for your approval after every step. The parts to tailor are marked `[FILL IN: ...]`.
- **Docs and examples** (`docs/`, `examples/`): templates, background research and a filled-in sample, so you can see the result before you start. Finnish translations are in `docs/fi/`.

A package can also be only a skill or a playbook without an agent. The packages work in any Claude Code project and need no other tools or external services.

## Roadmap

- **Planned:** more roles, skills and playbooks from a product team made of agents (for example a systems analyst, a QA role and the routines that connect them), published one package at a time. Each new package gets its own folder and its own page, and installs the same way.

## Review before use

These packages are prompts and instructions. Nobody has audited them, and they are provided as is. Read the agent and skill files before you use them, and check what they write into your project.

## Licence

[MIT](LICENSE). Copyright (c) 2026 Simo Parviainen.

## Author

Created by Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
