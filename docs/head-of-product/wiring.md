# Head of Product: wiring into the work rhythm

Ready text blocks for setup step 5. Pick the ones that fit the project's work rhythm and adapt them into the project's own commands, skills or instructions. The blocks are in English because they go into agent and command instructions.

The principle in all of them: the agent runs only at points where the owner really decides what is done next. Not per ticket, per pull request or per review. Multi-agent setups use many times more tokens. One sharp judgement at the right moment is worth more than constant commentary.

## A. Gate before the owner chooses the work (sprint planning or priority review)

```
### HEAD OF PRODUCT GATE (one run per planning point)

Runs after the candidate list is verified and before the owner chooses the scope, so the
value check happens before anyone spends time on scoping.

1. Skip check: if the work file for this round already has `HoP: run YYYY-MM-DD`, do not run
   it again; use that run's recorded summary.
2. Write the verified candidate list to a scratch file: candidates, carry-over, and any
   verification findings. Do NOT include the main session's own recommended shape; the agent
   must not anchor on it.
3. Start `head-of-product`. Give it the round number, the path of the candidate file, any
   metrics the main session already has that the agent cannot read itself, and the
   instruction: write pass 1 (own priorities from the strategy, decisions, backlog and latest
   work file) before opening the candidate file. Its report includes the retro on the
   previous round.
4. Dependency check by the main session: for every cut or defer it proposes, check what
   depends on it and flag any item a kept item depends on.
5. Anything the agent pulls in that was not on the list is verified before it is presented.

Present to the owner, in the owner's language, next to the candidate list: the agent's
strongest objection, its cut/defer list with the dependency flags, its independent priorities
where they differ, and its questions. The owner accepts or rejects each cut or defer. Record in
the work file: `HoP: run YYYY-MM-DD`, the owner's decision on each flag with its reason, and
for each deferred item a not-before date or a reason, so it is not re-raised every round. A
decision that changes strategy also goes to the decision log.
```

## B. Retro at the end of a round

```
### HEAD OF PRODUCT RETRO

At the close of a sprint or review period, before the next one is planned (if the next
planning runs the gate in A immediately, run it there instead, once):
- Did the round's work move the bets it was meant to? Name the metric and the number, or say
  that nobody measured, which is itself a finding.
- Which bets reached their kill-criterion date, and what does the criterion say now?
- During the trial (three rounds), fill in the trial tally with the owner: changed the owner's
  choice? a flag later proved right? the owner learned something new? (yes/no each)
```

## C. Idea check before building

```
### HEAD OF PRODUCT IDEA CHECK (offered, not automatic)

When the owner leans to building an idea now, or to adding it to the current round, offer one
short `head-of-product` run first: does it move a bet, what is its opportunity cost, the
cut/defer verdict, the strongest objection and the confidence. Run it only if the owner says
yes. Ideas going to the backlog or the idea list are checked at the next planning point anyway.
```

## D. Quarterly strategy review

```
### QUARTERLY STRATEGY REVIEW

Once a quarter, and whenever a bet's kill-criterion date passes:
- head-of-product reviews the strategy page against the quarter's results: diagnosis still
  right? bets moving? anything on "Not doing now" whose condition is now met? removals of
  little-used features?
- It proposes changes as a list; the owner decides each one; the main session updates the page
  and its "What changed" section, and refreshes the baselines.
```

## E. One line for the project's CLAUDE.md

```
- head-of-product runs only at [decision points]; never per ticket, per pull request, in QA or
  routine runs. Its anchor is `docs/product/strategy.md`; the owner decides every flag.
```
