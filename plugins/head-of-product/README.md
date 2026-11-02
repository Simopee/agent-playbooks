[Suomeksi](README.fi.md)

# Head of Product

When AI agents make building cheap, the hard question is what to build. This agent asks it at every planning point, against a strategy you wrote down.

## Install

```
/plugin marketplace add Simopee/agent-playbooks
/plugin install head-of-product@simopee-agent-playbooks
```

Then run `/head-of-product:setup` in your project.

**No install:** paste `https://github.com/Simopee/agent-playbooks` into Claude Code in your project and ask whether it would help your project.

## What it does

The package gives your project a Head of Product agent and a guided setup. The setup writes a one-page strategy with you: mission, primary user, a diagnosis of what holds the project back, 3-5 bets with metrics and kill criteria, a "Not doing now" list and decision rules. The agent then judges proposed work against that page at the points where you choose what to do next. It recommends what to keep, defer or cut, and why. You decide every flag.

## How it works inside

**Setup** (`/head-of-product:setup`, six steps, it stops for your approval after each):

1. **Mapping.** Claude reads your repository, records which parts of a strategy already exist, and finds your work rhythm (sprints or not, where you decide). Then it asks about the gaps, one question at a time.
2. **Strategy draft.** The agent drafts the page from the template. Every claim has a source or is marked as an assumption; unknown baselines are "not measured". It also drafts a page of what is known and what is only assumed about users.
3. **Review and lock.** You go through the draft section by section. When all are approved, the page is LOCKED with a date.
4. **Tailoring.** Claude copies the agent into your project (`.claude/agents/head-of-product.md`) and fills in the `[FILL IN: ...]` parts.
5. **Wiring.** Claude adds the agent to your decision points: a gate before you choose a round's scope, a retro at the end, an idea check before building, a quarterly strategy review. Text blocks exist for work with sprints and without.
6. **Trial.** Three rounds, three yes/no questions after each. Then you decide to keep, change or stop.

**Inputs:** your repository and your answers. **Outputs:** `docs/product/strategy.md`, `docs/product/users-known-vs-assumed.md` (in your language), a tailored agent, and a few lines in your project's instructions.

**How the agent works:** it writes its own priorities from the strategy first, before it reads the proposal, then lists the differences. This counters the tendency of language models to agree with the plan they are shown. It must name at least one thing to cut or defer, or say why nothing should go. It separates evidence from assumption and keeps its position unless it gets new evidence. It has no write access.

**Answer format** (at most about 700 words): independent priorities, differences from the proposal, cut/defer list, share of Leverage work, strongest single objection, evidence and confidence, at most three questions for you.

## Example

From [examples/head-of-product/sample-gate-result.md](../../examples/head-of-product/sample-gate-result.md) (a fictional project):

> **Strongest single objection.** The round polishes the product for readers while the diagnosis says readers leave because contents are stale. Nothing in it would change what a returning reader sees.

See also the [sample strategy page](../../examples/head-of-product/sample-strategy.md).

## Adapting it

The setup does the adapting with you. If you edit by hand, the parts to fill in are marked `[FILL IN: ...]` in `agents/head-of-product.md`: project description, anchor files, who owns order and capacity, growth lanes, data access and limits, decision points, and the list of things the agent may never decide in autonomous mode. Keep the working method; the background note explains why.

Docs: [wiring blocks](../../docs/head-of-product/wiring.md), [strategy template](../../docs/head-of-product/strategy-template.md), [users template](../../docs/head-of-product/users-template.md), [background and research](../../docs/head-of-product/background.md).

## Limits and review before use

- These are unaudited prompts, provided as is. Read them before use and check what the setup writes into your project.
- The agent cannot interview users or judge how an interface feels. At small scale its numbers are directional.
- It is built to run rarely, at decision points. Running it per ticket costs tokens and adds noise.

## Licence and author

MIT. Created by Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
