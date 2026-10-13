# CCAR-P practice questions

30 practice questions for **Claude Certified Architect - Professional** (CCAR-P), written for this repo and spread across the exam's seven domains by their official weights. 6 of them ask for more than one answer, as about a quarter of the real exam's questions do; those count only when every choice is right.

Choose your answer before you open the explanation.

**Prefer a timed run?** The [practice test](https://preporato.github.io/claude-certification-guide/#ccar-p) has the same questions, scores every domain, and runs in your browser.

| Domain | Exam weight | Questions here |
|---|---|---|
| Solution Design & Architecture | 17% | 5 |
| Claude Models, Prompting & Context Engineering | 13% | 4 |
| Integration | 19% | 6 |
| Evaluation, Testing & Optimization | 16% | 5 |
| Governance, Safety & Risk Management | 14% | 4 |
| Stakeholder Communication & Lifecycle Management | 14% | 4 |
| Developer Productivity & Operational Enablement | 7% | 2 |

---

### Question 1

*Solution Design & Architecture*

A support team wants answers to product questions grounded in a 300-page manual. Questions are single-turn, and the manual is updated monthly. What is the simplest sufficient architecture?

- **A.** An augmented LLM: retrieval over the manual feeding a single model call that cites the passages it used
- **B.** An autonomous agent that browses the manual page by page
- **C.** A multi-agent research system with a planner and three specialists
- **D.** A model fine-tuned on the manual every month

<details>
<summary>Answer</summary>

**A.** One well-scoped, grounded call meets the requirement, so retrieval plus a single call is the simplest sufficient pattern (A). C and B add autonomy the task doesn't need, with the cost and latency to match. Monthly fine-tuning (D) is heavy, slower to update than re-indexing, and gives no citations.

</details>

### Question 2

*Solution Design & Architecture*

Which architecture proposal for an invoice-processing assistant is complete?

- **A.** Extraction with schema validation; posting to the ERP; a dashboard of monthly volume
- **B.** Email intake and OCR; extraction with schema validation; posting to the ERP with an exceptions queue; per-field accuracy evals, user corrections and monitoring fed back into prompt and model decisions
- **C.** Email intake and OCR; extraction with the most capable model; posting to the ERP
- **D.** Email intake; a multi-agent extraction team; posting to the ERP; a launch announcement

<details>
<summary>Answer</summary>

**B.** A complete architecture has input, processing, output and a feedback loop that turns evals, user corrections and monitoring into design changes (B). C has no feedback loop. A has no input stage, and a volume dashboard measures activity without feeding quality back. D adds complexity and still has no feedback loop.

</details>

### Question 3

*Solution Design & Architecture*

Two designs meet the accuracy target. Design 1 uses the top tier: p95 latency 6 seconds, \$0.09 per request. Design 2 routes between the fast and balanced tiers: p95 latency 2 seconds, \$0.02 per request. The client's stated constraint is a 3-second p95 SLA at 2 million requests a month. Which design, and why?

- **A.** Run both in production indefinitely
- **B.** Postpone the decision until a newer model is released
- **C.** Design 1, for quality headroom
- **D.** Design 2, because it meets the latency SLA and the cost pillar at the same accuracy

<details>
<summary>Answer</summary>

**D.** When both options meet accuracy, the stated business constraint decides, and only Design 2 meets the 3-second SLA, at about \$40,000 a month against \$180,000 (D). C breaks the SLA. A doubles cost and complexity for no reason. B ignores a decision the data already supports.

</details>

### Question 4

*Solution Design & Architecture*

A due-diligence system must analyze each target company's financials, legal filings and press coverage. The three analyses are independent, and each needs different tools and sources. Which design fits?

- **A.** Three separate systems whose reports nobody combines
- **B.** One agent holding all the tools for all three analyses
- **C.** An orchestrator with three scoped subagents running in parallel, followed by a synthesis step
- **D.** One agent doing the three analyses in sequence

<details>
<summary>Answer</summary>

**C.** Independent subtasks with different tool needs are what justifies decomposition: each subagent gets a narrow toolset and its own context, and the orchestrator merges the results (C). B is capability bloat. D gives up parallelism and mixes three contexts. A skips the synthesis the client actually needs.

</details>

### Question 5

*Solution Design & Architecture*

A global retailer's policy assistant covers 14 regions. Each region's policies differ and are owned by different teams. Answers mix rules from different regions. What is the best design change?

- **A.** Put all 14 regions' policies in every request
- **B.** Partition by data domain: tag documents with their region and filter retrieval by the user's region before semantic search
- **C.** Fourteen agents that negotiate with each other on every question
- **D.** Ask users to mention their region and change nothing else

<details>
<summary>Answer</summary>

**B.** The data has a clean partition, so filtering on region metadata keeps other regions' rules out of the context (B). C adds coordination machinery to a retrieval problem. A is context stuffing. D leaves the mixed retrieval in place.

</details>

### Question 6

*Claude Models, Prompting & Context Engineering*

Which TWO workloads benefit most from prompt caching? (Select TWO)

- **A.** Single requests shorter than the minimum cacheable length
- **B.** Requests whose first line is the current timestamp
- **C.** An agent loop that resends the same 12,000-token system prompt and tool definitions on every turn
- **D.** An endpoint where many users ask questions about the same 50-page policy within minutes of each other
- **E.** A weekly job that sends one unique 3,000-token prompt

<details>
<summary>Answer</summary>

**C and D.** Caching pays off when a long, stable prefix repeats within the cache lifetime (C, D). A weekly unique prompt (E) never repeats in time. A timestamp at the start (B) breaks the prefix on every request. Prompts under the minimum length (A) are never cached.

</details>

### Question 7

*Claude Models, Prompting & Context Engineering*

An eligibility step must apply six interacting rules. Accuracy is the priority, and the latency budget is generous. Which prompting approach fits?

- **A.** A lower temperature
- **B.** Few-shot examples alone, with no stated rules
- **C.** Have the model reason through the rules step by step (or enable thinking) before deciding, with each rule stated as an explicit criterion, then validate the decision
- **D.** A zero-shot prompt kept as short as possible

<details>
<summary>Answer</summary>

**C.** Multi-step logic benefits from explicit reasoning before the answer, and the generous latency budget covers its cost (C). Zero-shot (D) suits simple, unambiguous tasks. Examples (B) teach format and edge cases, and six interacting rules still need to be stated. Temperature (A) adds no reasoning.

</details>

### Question 8

*Claude Models, Prompting & Context Engineering*

An enterprise assistant's system prompt has grown to 60,000 tokens of procedures for 40 business processes, and most requests need one or two of them. Latency and cost are high, and instruction-following has slipped. What is the best restructuring?

- **A.** Build 40 separate assistants and make users choose
- **B.** Move to a model with a larger context window
- **C.** Mark the most important procedures in capitals
- **D.** Keep the system prompt to the core role and rules, and package each procedure as a Skill or retrievable module that loads only when relevant

<details>
<summary>Answer</summary>

**D.** Loading procedures on demand keeps the context small and focused, which improves attention, cost and latency together (D). Emphasis (C) doesn't shrink the prompt. A bigger window (B) holds more of the same dilution. A moves the routing problem onto users.

</details>

### Question 9

*Claude Models, Prompting & Context Engineering*

Downstream systems consume the assistant's JSON, and occasional schema violations cause failed transactions. Which change addresses this at the source, and what still needs checking?

- **A.** Structured outputs with the integration schema, which guarantees schema-valid JSON, plus semantic validation of the values and handling of the refusal and `max_tokens` stop reasons
- **B.** A stronger instruction to follow the schema
- **C.** A retry loop and nothing else
- **D.** A regex that repairs broken JSON

<details>
<summary>Answer</summary>

**A.** Constrained decoding removes schema violations at the source, and semantic checks plus stop-reason handling cover what it doesn't guarantee (A). Retries (C) and instructions (B) reduce failures without eliminating them. Regex repair (D) guesses at intent and can corrupt data quietly.

</details>

### Question 10

*Integration*

A procurement agent must get quotes from a supplier's own AI agent, which runs on the supplier's systems with its own tools, policies and reasoning. Which integration mechanism fits?

- **A.** Agent-to-agent delegation over a defined protocol, with explicit request and response contracts, authentication, and failure isolation
- **B.** A direct API call to Claude with the supplier's price list pasted into the prompt
- **C.** An MCP server that gives your agent direct access to the supplier's database
- **D.** A shared system prompt that both companies edit

<details>
<summary>Answer</summary>

**A.** Two autonomous systems with separate owners, tools and policies call for delegation between agents, with contracts and isolation so either side can fail independently (A). C bypasses the supplier's agent and policies and assumes access you won't get. B works only if you already have current prices, which is what you're asking for. D merges two organizations' control into one prompt.

</details>

### Question 11

*Integration*

One internal app sends support tickets to Claude for tagging. One team owns it, and no reuse is planned. A platform engineer proposes building an MCP server first. What is the right assessment?

- **A.** Fine-tune a tagging model instead
- **B.** Build the MCP server, since every integration should use MCP
- **C.** Use a direct API integration now; MCP adds a protocol layer and maintenance without a reuse need, so revisit it if other surfaces need the capability
- **D.** Use agent-to-agent delegation

<details>
<summary>Answer</summary>

**C.** MCP pays off when one capability serves many clients or surfaces, and one app with one owner is the direct-API case (C). B adds maintenance for a benefit that doesn't exist yet. D adds autonomous-system machinery to a single call. A skips a simpler option that works.

</details>

### Question 12

*Integration*

Which TWO observations are signs of capability bloat in a production agent? (Select TWO)

- **A.** Two tools have overlapping descriptions, and both plausibly handle 'find a customer'
- **B.** Each subagent's tools are scoped to its responsibility
- **C.** The reporting agent uses read-only credentials
- **D.** It exposes 45 tools, and invocation logs show only 9 ever used
- **E.** Tool descriptions state when not to use each tool

<details>
<summary>Answer</summary>

**A and D.** Unused tools that ship with every request (D) and overlapping tools that blur selection (A) are classic signs of bloat. Scoped toolsets (B), read-only credentials for a read-only job (C) and boundary statements in descriptions (E) are the cure.

</details>

### Question 13

*Integration*

An agent connects to six MCP servers exposing 300 tools, and every request front-loads all of their definitions. Tool selection is poor and costs are high. What is the best fix?

- **A.** Add more examples to the system prompt
- **B.** Shorten every tool description to one line
- **C.** Move to a model with a larger context window
- **D.** Progressive discovery: load tool definitions on demand (for example with tool search and deferred loading), and give each agent only the servers its responsibility needs

<details>
<summary>Answer</summary>

**D.** Loading tools as the agent narrows in cuts tokens and improves selection accuracy, and scoping servers per responsibility removes tools that never belonged (D). A bigger window (C) holds the same noise. One-line descriptions (B) make selection worse. Examples (A) add tokens without reducing the tool count.

</details>

### Question 14

*Integration*

A company assistant answers questions over the document store using a service account that can read every folder, including HR and legal. A contractor asked about salaries and got an answer. What is the root fix?

- **A.** Remove HR documents from the index
- **B.** Run retrieval and tools with the calling user's identity and permissions, and attribute every access to that user in the logs
- **C.** Add a system-prompt rule: 'Never discuss salaries'
- **D.** Filter out responses that contain the word 'salary'

<details>
<summary>Answer</summary>

**B.** The shared over-privileged account erased per-user authorization and made every access unattributable, so the fix is acting as the caller (B). C is a probabilistic patch, A breaks legitimate HR use, and D is easy to get around and blocks legitimate answers.

</details>

### Question 15

*Integration*

Engineers search an internal knowledge base with exact error codes such as 'E-4031.' Semantic search returns conceptually similar documents about other errors. What is the best fix?

- **A.** A larger embedding model
- **B.** Hybrid search: keyword matching for exact identifiers combined with semantic search, then re-ranking
- **C.** Retrieve more chunks per query
- **D.** Fine-tune the generation model on error codes

<details>
<summary>Answer</summary>

**B.** Exact identifiers such as error codes and SKUs need keyword matching, which hybrid search adds alongside semantic retrieval (B). Better embeddings (A) still treat codes as fuzzy meaning. More chunks (C) add noise. The generation model (D) can't fix documents that were never retrieved.

</details>

### Question 16

*Evaluation, Testing & Optimization*

A contract-extraction service has three complaints: wrong values, slow responses at peak hours, and a rising monthly bill. Which THREE metrics should the monitoring plan track? (Select THREE)

- **A.** Field-level accuracy against a labeled dataset
- **B.** Average response length
- **C.** p95 and p99 latency
- **D.** Number of prompt revisions per month
- **E.** Cost per document and tokens per task

<details>
<summary>Answer</summary>

**A, C, E.** Each complaint maps to a metric: wrong values to accuracy (A), slowness to tail latency (C), and the bill to cost per unit of work (E). Prompt revision counts (D) and response length (B) measure activity, and neither shows whether the complaints are fixed.

</details>

### Question 17

*Evaluation, Testing & Optimization*

A team tuned its prompt against the same 200 examples it uses to report accuracy. Testing shows 98%, and production shows 84%. What went wrong, and what is the fix?

- **A.** The eval set leaked into prompt development and inflated the score; tune on a separate development set and report on a held-out set that mirrors production
- **B.** The model is too small; upgrade the tier
- **C.** Production traffic is low quality; filter it
- **D.** 200 examples is too few; add 20 more of the same kind

<details>
<summary>Answer</summary>

**A.** Tuning against the test set overfits to it, so the score stops predicting production (A). C blames the data the system has to handle. B changes the model without fixing the measurement. D keeps the same leak with a slightly bigger set.

</details>

### Question 18

*Evaluation, Testing & Optimization*

A team wants to ship a new prompt, new retrieval settings and a tier change together, because 'it felt better in 15 spot checks.' What is the correct approach?

- **A.** Run 15 more spot checks
- **B.** Ask the stakeholders which version they prefer
- **C.** Test one variable at a time with a success metric and sample size set in advance, then ship each change only on a significant result
- **D.** Ship all three, since the spot checks were positive

<details>
<summary>Answer</summary>

**C.** A clean experiment changes one variable and decides on a metric chosen in advance (C). With three changes at once (D), a win or a loss can't be attributed to anything. Preference (B) and more spot checks (A) are still the feels-better method.

</details>

### Question 19

*Evaluation, Testing & Optimization*

Traces show the correct policy passages are retrieved, yet answers still state the wrong refund window. Where is the failure, and what is the first fix?

- **A.** Raise the number of retrieved passages
- **B.** The index is stale: rebuild it
- **C.** Retrieval failure: re-chunk and re-embed the corpus
- **D.** Generation is poorly grounded: tighten the instructions to answer only from the retrieved passages and cite them, and evaluate faithfulness

<details>
<summary>Answer</summary>

**D.** When the right documents arrive and the answer is still wrong, the failure sits in generation and grounding (D). C and B fix retrieval, which the traces show is working. A adds noise to a context that already contains the answer.

</details>

### Question 20

*Evaluation, Testing & Optimization*

Answers about leave policies leave out exceptions. Traces show the retrieved chunks contain the rule sentence, while the exception sits in the next paragraph, which isn't retrieved. What is the best fix?

- **A.** Retrieve 30 chunks instead of 5
- **B.** Move to a more capable model
- **C.** Tell the model to remember that policies have exceptions
- **D.** Re-chunk along the document's structure (whole sections) with some overlap, so rules and their exceptions stay together

<details>
<summary>Answer</summary>

**D.** Chunks smaller than the unit of meaning split rules from their qualifiers, so structure-aware chunking fixes the retrieval unit (D). More chunks (A) might catch the exception along with plenty of noise. No model (B) can use a paragraph it never receives, and an instruction (C) can't supply the missing text.

</details>

### Question 21

*Governance, Safety & Risk Management*

An agent reads inbound customer emails and can issue refunds. Which TWO controls are deterministic, as opposed to prompt-based? (Select TWO)

- **A.** An output filter that blocks any reply containing a full account number
- **B.** Few-shot examples of the agent declining suspicious requests
- **C.** A system-prompt rule: 'Never issue large refunds'
- **D.** A persona instruction: 'You are a careful agent'
- **E.** Tool permissions that cap a refund at \$100 per call and send larger amounts for human approval

<details>
<summary>Answer</summary>

**A and E.** Permission limits (E) and output filtering (A) are enforced in code, whatever the model decides. C, D and B shape behavior probabilistically, and a cleverly written email can talk the model past them.

</details>

### Question 22

*Governance, Safety & Risk Management*

A moderation pipeline handles 500,000 low-risk comments a day and occasionally receives legal threats. Which human-in-the-loop design fits?

- **A.** Have a human review every comment
- **B.** Automate routine decisions with sampled QA, and route legal threats and cases below system-set thresholds to human reviewers
- **C.** Remove humans entirely
- **D.** Let the model escalate whenever its self-reported confidence is low

<details>
<summary>Answer</summary>

**B.** Humans go where the risk is high, and sampling covers the routine volume (B). Reviewing everything (A) destroys the efficiency case. C leaves legal threats unhandled. Self-reported confidence (D) is poorly calibrated, so the thresholds have to be set by the system.

</details>

### Question 23

*Governance, Safety & Risk Management*

A US telehealth company with patients in the US and Germany plans to use Claude to summarize clinical notes. Which TWO frameworks apply? (Select TWO)

- **A.** FedRAMP
- **B.** HIPAA, for US patients' health information
- **C.** GDPR, for the personal data of patients in the EU
- **D.** None, since Claude is a third-party service
- **E.** Only HIPAA, since the company is based in the US

<details>
<summary>Answer</summary>

**B and C.** The framework follows the data type and the jurisdiction: US health data brings HIPAA (B), and processing EU residents' personal data brings GDPR wherever the company is based (C). FedRAMP (A) covers cloud services for US federal agencies. E ignores the German patients, and D confuses using a vendor with being exempt.

</details>

### Question 24

*Governance, Safety & Risk Management*

Your observability stack stores full prompts and responses, including customer personal data, in a log platform that 300 engineers can read. What is the risk, and what is the fix?

- **A.** Data leakage through logs: redact personal data before logging, restrict access to the people who need it, and set a retention limit
- **B.** Ask the model to leave personal data out of its responses
- **C.** Encrypt the stored logs and leave access as it is
- **D.** No risk, because the logs are internal

<details>
<summary>Answer</summary>

**A.** Logs and traces are a leakage channel, so the fix minimizes what's stored and who can see it (A). Internal access (D) still exposes customer data to hundreds of people. Encryption with unchanged access (C) protects the storage while every reader still sees the data. B leaves the personal data in the prompts, and the model can't be relied on to keep it out of responses.

</details>

### Question 25

*Stakeholder Communication & Lifecycle Management*

A vice president asks you to 'make customer support better with AI.' What should you produce first?

- **A.** A comparison of model benchmark scores
- **B.** A working prototype to show next week
- **C.** Discovery outputs: a measurable success criterion, a constraint inventory, a data and access map, a stakeholder map with decision owners, and a baseline of the current process
- **D.** A signed vendor contract

<details>
<summary>Answer</summary>

**C.** Professional engagements start with discovery, because every later design choice depends on what success means and which constraints apply (C). A prototype (B) built without discovery answers a question nobody has defined. Benchmarks (A) and contracts (D) come after the requirements are known.

</details>

### Question 26

*Stakeholder Communication & Lifecycle Management*

Stakeholders ask for a guarantee that the assistant 'never gives a wrong answer.' What is the appropriate response?

- **A.** Commit only to 99.9% uptime
- **B.** Promise 100% accuracy to secure approval
- **C.** Refuse to set any accuracy target
- **D.** Commit to measured targets, such as at least 96% accuracy per slice on a held-out set with an error budget, escalation paths and a remediation plan, and explain that LLM outputs have a measurable error rate

<details>
<summary>Answer</summary>

**D.** Probabilistic systems get SLAs built on measured rates, error budgets and remediation (D). B sets up a broken promise. C leaves stakeholders nothing to hold the system to. Uptime (A) says nothing about answer quality.

</details>

### Question 27

*Stakeholder Communication & Lifecycle Management*

Which statement best communicates a model-tier recommendation to business stakeholders?

- **A.** 'We chose the newest model available.'
- **B.** 'The top tier scores higher on industry benchmarks.'
- **C.** 'The balanced tier resolves 91% of tickets at \$0.02 each, and the top tier resolves 93% at \$0.08. At a million tickets a month, the extra two points cost about \$60,000 a month, so we recommend the balanced tier with escalation for complex tickets.'
- **D.** 'The balanced tier is fine.'

<details>
<summary>Answer</summary>

**C.** Architect-level communication puts the trade-off in business terms: outcome, cost, and the recommendation that follows from them (C). B is engineering language with no business meaning. D gives no basis for the decision, and A offers novelty as a reason.

</details>

### Question 28

*Stakeholder Communication & Lifecycle Management*

Which TWO artifacts belong in the handoff to the team that will operate the system? (Select TWO)

- **A.** The architect's personal working notes
- **B.** The kickoff slide deck
- **C.** A raw export of the project chat channel
- **D.** Runbooks covering escalation paths and known failure modes
- **E.** Eval baselines and an inventory of prompts and their versions

<details>
<summary>Answer</summary>

**D and E.** Operators need to know how to respond to problems (D) and what normal looks like, along with what is deployed (E). Personal notes (A), kickoff slides (B) and raw chat (C) aren't operational documentation.

</details>

### Question 29

*Developer Productivity & Operational Enablement*

Claude Code runs in your CI pipeline, and the team agrees it must never run git push or curl anywhere the repository is used. Where should this restriction live?

- **A.** Each developer's `~/.claude/settings.json`
- **B.** Deny rules in the committed project settings, such as `Bash(git push *)` and `Bash(curl *)`, which the client enforces
- **C.** A wiki page
- **D.** A `CLAUDE.md` instruction

<details>
<summary>Answer</summary>

**B.** Permission rules in version-controlled project settings apply everywhere the repository runs, CI included, and the client enforces them (B). User settings (A) don't reach CI or other developers. `CLAUDE.md` (D) is guidance the model weighs. A wiki (C) is invisible to the tooling.

</details>

### Question 30

*Developer Productivity & Operational Enablement*

A platform team built a code-review subagent and a release-notes skill that every repository in the company should use, in the same version. What is the best way to distribute them?

- **A.** Package them as a plugin (or deploy them through managed settings), so every developer gets the same versioned definitions
- **B.** Post the prompt text in a chat channel for developers to copy
- **C.** Ask each developer to copy the files into `~/.claude/`
- **D.** Paste both into every repository's `CLAUDE.md`

<details>
<summary>Answer</summary>

**A.** Plugins bundle skills and subagents for distribution, and managed settings can push them to the whole organization, which keeps one maintained version (A). Copy-and-paste distribution (B, C) drifts as soon as the originals change. `CLAUDE.md` (D) holds always-on instructions and can't define a subagent or an on-demand skill.

</details>

---

## Where to go next

- **Review by domain.** If your misses cluster, re-read those domains in Part II of the [CCAR-P study guide](./guide.md):
  - [Solution Design & Architecture](./guide.md#domain-1-solution-design--architecture-17)
  - [Claude Models, Prompting & Context Engineering](./guide.md#domain-2-models-prompting--context-engineering-13)
  - [Integration](./guide.md#domain-3-integration-19)
  - [Evaluation, Testing & Optimization](./guide.md#domain-4-evaluation-testing--optimization-16)
  - [Governance, Safety & Risk Management](./guide.md#domain-5-governance-safety--risk-14)
  - [Stakeholder Communication & Lifecycle Management](./guide.md#domain-6-stakeholder-communication--lifecycle-14)
  - [Developer Productivity & Operational Enablement](./guide.md#domain-7-developer-productivity--enablement-7)
- **Practice at full length.** The [CCAR-P page on Preporato](https://preporato.com/certificates/claude-certified-architect-professional) has free sample questions and six full-length timed practice tests (paid) in the exam's format, with a score for every domain.

Found a mistake in a question? [Open an issue](https://github.com/preporato/claude-certification-guide/issues/new?template=outdated-fact.yml) and we'll fix it.

*These questions were written for this repo and are not taken from the exam. Not affiliated with Anthropic.*
