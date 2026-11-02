# Strategy page template

This file gives the structure and the guidance. The real page is written to `docs/product/strategy.md` in your project (or the path chosen in setup step 1), in the owner's language. Remove the guidance text (in italics) from the finished page.

Light means: one page, 3-5 bets, 5-7 decision rules. The page grows in reviews as use shows a need. Decision rules accumulate over months of use; do not write them all at once.

---

# [Project name]: strategy

> **Status: DRAFT** (changed to "LOCKED YYYY-MM-DD" once the owner has approved the page section by section). Changes only by the owner's decision. The Head of Product proposes.

## Mission

*One or two sentences: what the project does and for whom. Quote the owner if they have said it themselves. Then add two or three sentences on what follows from the mission: what is the core and what is a supporting feature.*

## Primary user

*Who uses it and in what situation. Where they come from (search, recommendation, direct), on which device, what they want to get done. If there is a smaller but valuable group, name it separately and say that features built for it are weighed by the group's size.*

## Business model (if relevant)

*Free, paid, revenue from elsewhere, the goal (for example a sale or recurring income). Only what steers prioritisation. If this section contains something that must not be used publicly, say so here.*

## Diagnosis: what is holding us back now (date)

*The most important section. Write it before the bets. What are the one or two things that now stop the project from moving forward? Name an obstacle; a list of goals is not a diagnosis. Every claim has a source (metric, file, the owner's word) or is marked as an assumption. End with "To verify": what in the diagnosis is inference rather than tested, and how it will be tested.*

*Example of the shape: "Search visibility holds growth back. The pages work, but the search engine leaves part of them unindexed (source: search console, date). To verify: the cause is an inference; test it by pruning weak pages and following indexing for 8 weeks."*

## Guiding policy

*One principle that follows from the diagnosis and guides choices for the next months, and 2-4 things that follow from it. If the owner has made a conscious choice that does not follow from the diagnosis, write it down and say why it was made.*

## Bets (period)

*A bet is a bounded piece of work that gets time because we believe it moves a goal. Only work that moves some bet is taken on. 3-5 bets. For each:*

### Bet 1. [name]

- **Metric:** *how we see whether the bet is moving. Source and frequency.*
- **Actions:** *what is done in this period.*
- **Kill criterion:** *a state and a date: "if X is not at Y by date Z, the bet is stopped or re-evaluated". If the criterion cannot be set yet, write when it will be set (for example after the first measurement).*

## Not doing now

*Things that are not done in this period, even if they may be good ideas. Each with a reason and the condition under which it can be reconsidered. A good idea that relates to no bet goes to the idea list to wait for the review.*

1. *[item]. [reason]. Reconsider when [condition].*

## Decision rules

*The Head of Product judges work by these rules. Start from these seven, adapt them to the project and delete the ones that do not fit. Add new ones only when use shows the need.*

1. **Every piece of work relates to a bet.** Otherwise it goes to the idea list.
2. **Opportunity cost.** The question is not "is this worth doing" but "is this the best use of the next slot".
3. **Decided but not done.** Approved decisions that nobody is building are raised every time.
4. **Kill criterion before starting.** Every bet and experiment has a state and a date at which it is stopped or re-evaluated.
5. **For whom and how many.** For every feature, ask whether it serves most users or a small group.
6. **Simplicity.** For every addition, ask: which task does it serve, what does it cost in the user's attention, what could be removed instead, and can it be done with what already exists.
7. **A small number is not evidence, and the owner decides.** No decision rests on small numbers alone. "I don't know" is an acceptable answer. The Head of Product recommends, the owner decides, and a rejected flag does not return without new evidence.

## Metrics and baselines

| Metric | What it tells | Source and frequency | Baseline (date) |
|---|---|---|---|
| *[metric]* | *[what it tells]* | *[source, frequency]* | *[number or "not measured"]* |

*Finally, record the limits of measurement: what the numbers do not tell, where part of the traffic or use is missing, which numbers are too small for decisions.*

## Maintenance

- The page is reviewed quarterly. First review: [date].
- Also whenever a bet's kill-criterion date passes.
- Only the owner changes the page. The Head of Product proposes.

## What changed

- *[date]: page written and locked (decision [id]).*
