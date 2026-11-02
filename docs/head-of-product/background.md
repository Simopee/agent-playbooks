# Head of Product agent: background and rationale

The agent was first built for a product run by one non-developer owner with a team of AI agents, then generalised. Project-specific choices are removed; the research and the reasoning behind the agent's working method are kept, because they are what makes the agent useful rather than agreeable.

Tags: **[source]** a cited source supports it, **[secondary]** only summaries were reachable, **[inference]** reasoning.

## 1. Good vs great Head of Product

| Good | Great | Source |
|---|---|---|
| Prioritises the backlog well | Sets problems to solve tied to an outcome; the roadmap is a consequence | Cagan, https://www.svpg.com/product-vs-feature-teams/ |
| Measured by shipping | Measured by the outcome moving | Cagan, same |
| Tracks many initiatives | Picks the vital few and writes down "all the things you won't do" | Cagan, https://www.svpg.com/product-strategy-overview/ |
| Puts out fires | Anticipates the serious flaws | Horowitz, https://a16z.com/2012/06/15/good-product-managerbad-product-manager/ |
| Gives verbal opinions | Takes written positions and owns failures | Horowitz |
| Asks "is the return positive?" | Asks "is this the best use of the next slot, against everything else?" (opportunity cost) | Doshi [secondary], https://www.lennysnewsletter.com/p/episode-3-shreyas-doshi |
| Works hard on everything | Separates Leverage / Neutral / Overhead work (LNO) and spends care on Leverage | Doshi [secondary] |
| Treats slow progress as an execution problem | Checks first whether it is a strategy problem | Doshi [secondary] |
| Ships and moves on | Ships, measures, iterates, removes; runs a retro on past bets | Cutler, https://cutle.fish/blog/12-signs-youre-working-in-a-feature-factory |
| Takes the first good idea forward | Compares at least three solutions per opportunity, tests the riskiest assumption | Torres, https://www.producttalk.org/opportunity-solution-trees/ |
| Sets ambitious goals | Writes a diagnosis of the core obstacle, then a guiding policy, then coherent actions | Rumelt [secondary] |
| Lists features | States a hypothesis with a metric and tactics | Biddle, https://askgib.substack.com/p/ask-gib-how-do-all-your-product-strategy |
| Defines the "how" | Defines the "what" and "why", leaves the "how" to the builders | Horowitz |
| Starts work and hopes | Sets kill criteria (state + date) before starting; pre-mortem before big bets | Annie Duke / Doshi [secondary] |

**Feature-factory drift signs (Cutler) most relevant to a small AI-built project [inference]:** shipping celebrated without measured impact; nothing is ever cut or removed; roadmap items are features, not outcomes; no retro on whether bets paid off; shiny objects crowd out product health.

**Local optimisation smell [inference on LNO]:** most of a round is Neutral or Overhead work (copy tweaks, small interface polish, refactors) while the Leverage work sits in the backlog. This is the drift the agent is built to catch.

**Thin data [inference]:** at small scale, analytics is directional and A/B tests are underpowered. Lean on search query data, a few real user conversations and feedback; use leading proxies; set bets with state-and-date kill criteria instead of significance tests; prefer cheap, reversible experiments. Simulated personas test comprehension, never demand.

**Strategy page format.** Rumelt's kernel: diagnosis, guiding policy, 3-5 coherent actions, plus a not-doing list. Cagan: vision stable, strategy flexible. Biddle's "get big on something small, lead, expand": raise sequencing questions when expansion starts before the core is proven.

**What does not transfer to a solo owner with AI agents:** hiring and coaching, team topology, stakeholder politics (the only stakeholder is the decider), status reporting, sales-driven features (the analogue is "one user asked for it"), the product trio.

## 2. How LLM agents fail in an advisory role, and what counters it

This part is why the template's working method is not to be removed in tailoring.

| Failure | Evidence | Countermeasure in the template |
|---|---|---|
| Sycophancy: endorses the plan or framing it is shown | https://arxiv.org/abs/2310.13548, https://arxiv.org/abs/2505.13995, https://openai.com/index/sycophancy-in-gpt-4o/ | Mandatory cut/defer output; "agreement is not the goal" |
| Drops correct positions under "are you sure?" | https://arxiv.org/abs/2311.08596 | Recommendation written before the human reacts; change only on new evidence, named |
| Overconfident, claims without data | https://arxiv.org/abs/2306.13063 | Evidence vs assumption split; "I don't know" allowed; "what would change my mind" |
| Invents user insight; a persona title adds tone, not knowledge | https://arxiv.org/abs/2311.10054 | Procedure, not persona; every user claim cites a source or is labelled an assumption |
| Anchors on the first framing | https://arxiv.org/abs/2412.06593 | Independent pass first from strategy and data, then the proposal, then differences |
| Rubber-stamps other agents; prefers longer answers | https://arxiv.org/abs/2306.05685, https://arxiv.org/abs/2404.13076 | Fixed output; length cap; separate context, not a "devil's advocate" label |
| Debate adds little over independent samples | https://arxiv.org/abs/2310.01798 | No multi-round debates; one independent pass |
| Token use in multi-agent setups | https://www.anthropic.com/engineering/multi-agent-research-system | Runs only at real decision points, never per ticket |
| Role inflation when it designs its own role; drift between sessions | [inference] | The owner defines the role; the locked strategy page is the persistent anchor |

## 3. What is generic and what is tailored

**Generic, kept as is:** the role boundary (what and why, never how), the two-pass method, the standard questions, the evidence rules, holding position, the fixed output and its length cap, autonomous mode only on a locked strategy, the never list.

**Tailored per project (setup step 4):** the project description, the anchor files, the boundary with whoever owns order and capacity, the growth lanes, data access, scale and its limits, the decision points and work rhythm, at most two project-specific questions, the parked list for autonomous mode.

**Built with the project (setup steps 2-3):** the strategy page. If a project already has a strategy page, the agent's first job is to hold the work to it and propose the missing parts (diagnosis, bets with kill criteria, the not-doing list). In a project without one, writing it is the first job, and the owner locks it section by section before the agent judges anything against it.

## 4. Trial

The setup ends with a trial of three rounds and three yes/no questions per round: did the agent change the owner's choice, did a flag later prove right, did the owner learn something new. No public trial results are published yet.
