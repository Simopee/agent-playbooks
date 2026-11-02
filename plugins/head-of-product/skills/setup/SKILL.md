---
name: setup
description: Guided setup of the Head of Product agent in the current project, with a light written strategy for it to judge against. Six steps (mapping, strategy draft, review and lock, tailoring the agent, wiring into the work rhythm, trial), stopping for the owner's approval after each. Use when the user asks to set up, install or start the Head of Product agent.
---

Original work by Simo Parviainen, github.com/Simopee/agent-playbooks, MIT License.

# Set up the Head of Product agent and a light strategy

This skill brings the Head of Product agent into the current project. At the same time it writes a light strategy for the project, because the agent judges everything against it. Without a written strategy the agent either invents its own or agrees with whatever it is shown. Neither helps.

## Files this skill uses

The plugin's files are under `${CLAUDE_PLUGIN_ROOT}`. If you are reading this file outside an installed plugin (for example from the GitHub repository), the same files are under `plugins/head-of-product/` in that repository.

- Agent template: `${CLAUDE_PLUGIN_ROOT}/agents/head-of-product.md`
- Strategy page template: `${CLAUDE_PLUGIN_ROOT}/skills/setup/references/strategy-template.md`
- Users template: `${CLAUDE_PLUGIN_ROOT}/skills/setup/references/users-template.md`
- Wiring blocks: `${CLAUDE_PLUGIN_ROOT}/skills/setup/references/wiring.md`
- Background and rationale: `${CLAUDE_PLUGIN_ROOT}/skills/setup/references/background.md`

Before step 1, read this whole file and the background note, so you know why the agent is built the way it is.

## How you work in this skill

- Go step by step. After each step, stop and wait for the owner's approval. The next step starts only when the owner has approved the previous one.
- Before the mapping is approved, do not write the strategy, do not edit the agent and do not change the project's processes.
- Talk to the owner in their language, plainly, one question at a time. When you propose something, give your recommendation and its reason.
- Repository files and agent instructions are in English. The strategy page, the users file and everything the owner reads are in the owner's language.
- Never overwrite an existing file with the same name. If a target file already exists, tell the owner and ask.

## Who does what

- **The owner** (the person who decides what gets built) decides everything: the content of the strategy, locking it, the agent's role, and where the agent is wired in. The agent recommends, the owner decides.
- **The main session** (you, the Claude the owner talks to) runs the process, writes the files and starts the agents. The Head of Product agent has no write access.
- **An analyst agent**, if the project has one, maps the project's structure and ways of working. If not, you do it yourself.
- **The Head of Product** writes the strategy draft and later judges work against it.

## Default file locations in the project

- Strategy page: `docs/product/strategy.md`
- Users file: `docs/product/users-known-vs-assumed.md`
- Tailored agent: `.claude/agents/head-of-product.md`

If the project already keeps product documents elsewhere, propose that location in step 1 and use what the owner approves.

## Step 1. Mapping

Goal: know what has already been written about the project and what is missing, before asking the owner anything.

Read the repository: README, `CLAUDE.md`, memory files, decision log, backlog or ticket list, the latest sprint or work files, product documents, sources of analytics and metrics, and the commits of the last few weeks. For each section of the strategy page (see the strategy template), record one of:

- **Found:** where, with a quote or a summary.
- **Partly:** what is there and what is missing.
- **Missing.**

Also record the project's **work rhythm**, because step 5 decides from it where the agent is wired in:

- Are sprints used? If so, how long, and is there a ritual or command for opening and closing a sprint?
- If there are no sprints, how is work chosen? A continuous flow of tickets, work as ideas come, a monthly review, releases, or something else?
- At which points does the owner really decide what is done next? Those are the agent's natural places.
- What metric data is available and how (analytics, search engine data, database, user feedback)? What can the agent read itself and what must the main session hand to it?

Tell the owner the result briefly: what was found, what is missing, and what the work rhythm is. Then ask about the gaps **one question at a time**, most important first. Do not ask what the repository already tells you. The most important gaps are usually these: what the project is for and for whom, what is holding it back now, what the next months should be spent on, and what the owner does not want to do.

**Stop 1:** the owner approves the mapping and answers the gaps.

## Step 2. Strategy draft

Start the Head of Product agent from the plugin (`head-of-product:head-of-product`) to write the draft in the shape of the strategy template. The agent is not tailored yet and stops by design, except for this step: tell it explicitly that this is setup step 2 and it is writing the strategy draft, and give it the mapping, the owner's answers, the paths of the project files and the path of the strategy template. If the agent still stops, write the draft yourself by the same rules and say so to the owner. Save the draft to the strategy page path with the status DRAFT, in the owner's language.

Rules for the draft:

- **Light.** One page. 3-5 bets, 5-7 decision rules. The page grows later in reviews, when use shows the need.
- **Diagnosis first.** Before the bets, write what is really holding the project back now. The bets follow from the diagnosis. A list of goals without a diagnosis is not a strategy.
- **Every claim has a source** (file, metric, the owner's answer) or is marked as an assumption.
- **No invented numbers.** If a baseline is not known, write "not measured" and propose how to measure it.
- **A kill criterion for every bet:** a state and a date at which the bet is stopped or re-evaluated. If it cannot be set yet, write when it will be set.

The Head of Product also writes the first version of the users file (from the users template): what is known about users and what is only assumed.

**Stop 2:** present the draft to the owner as a short summary in their language.

## Step 3. Review and lock

Go through the draft with the owner **one section at a time**. For each: what the draft says, what it rests on, and what the alternatives were. The owner approves, changes or deletes. Record the changes at once.

When every section is approved, change the page's status to **LOCKED** with the date, and record the decision in the project's decision log (create one if the owner wants it). Only the owner changes a locked page. The Head of Product proposes changes.

**Stop 3:** the strategy is locked.

## Step 4. Tailoring the agent

Copy the agent template to `.claude/agents/head-of-product.md` in the project and rewrite it for the project. Every part to fill in is marked `[FILL IN: ...]`. Keep the template's structure and working method: two passes (own view first, then the comparison), the mandatory cut list, the split between evidence and assumption, holding position without new evidence, the fixed answer format and the length limit. Do not remove these in tailoring, because they are why the agent does not just agree (background note, part 2). Keep the attribution line. Remove the template-status block and the "Untailored" sentence from the description.

Tailor:

- The project description in the first paragraph.
- The anchor files: the path of the locked strategy, the decision log, the backlog, the work files.
- Boundaries with other agents or people: who decides order and capacity (for example an analyst agent, or the owner), who owns design, copy and legal.
- The project's growth lanes ("big picture") from the strategy page.
- Data: what the agent may read itself (read-only) and what the main session hands to it.
- The work rhythm and the decision points, from the step 1 mapping and the step 5 decision.
- The model: the strongest available, because the role is judgement and it runs rarely.

The project copy loads as `head-of-product`. From now on use that one, not the plugin's template (`head-of-product:head-of-product`).

**Stop 4:** the owner approves the agent. Show them the changes against the template briefly, in their language.

## Step 5. Wiring into the work rhythm

The agent runs **only at decision points**, never per ticket, per pull request or per review. Choose the wiring from the work rhythm found in step 1. The ready text blocks are in the wiring file.

| Work rhythm | Wiring |
|---|---|
| Sprints with an opening and closing ritual | Gate (A) in sprint planning before the owner decides the content; retro (B) at sprint close; idea check (C); quarterly review (D) |
| Sprints without a ritual | Light gate (A) at sprint start (the owner asks or the main session offers); retro (B) at sprint end; idea check (C); quarterly review (D) |
| Continuous flow, no sprints | Regular priority review with the gate (A), for example every two weeks or monthly; idea check (C) before work starts; quarterly review (D) |
| Work from ideas as they come | Idea check (C) before building; a monthly review of whether any bet moved (B); quarterly review (D) |

If the rhythm is something else, propose to the owner 2-3 points where they really choose what is done next. Those are the agent's places.

Add the chosen blocks to the project's own commands, skills, instructions or `CLAUDE.md`. Add one line to the project's `CLAUDE.md` (block E): where the agent is used and where it is not.

**Stop 5:** the owner approves the wiring.

## Step 6. Trial period

The agent is on trial for three rounds (three sprints or three reviews). After each round, record three questions with the owner:

1. Did the agent's judgement change the owner's choice? yes / no
2. Did one of the agent's flags later prove right? yes / no
3. Did the owner learn something new they would not have noticed otherwise? yes / no

After three rounds the owner decides: continue, change or stop. Three "no" answers on all three rounds mean the agent is an expensive way of saying what the owner already knows.

## Maintenance

- The strategy page is reviewed quarterly, and whenever a bet's kill-criterion date passes.
- A rejected flag does not return without new evidence.
- The agent does not expand its own role. If it proposes a change to its role, the owner decides.
