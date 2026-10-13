# CCAO-F practice questions

30 practice questions for **Claude Certified Associate - Foundations** (CCAO-F), written for this repo and spread across the exam's seven domains by their official weights. 6 of them ask for more than one answer, as about a quarter of the real exam's questions do; those count only when every choice is right.

Choose your answer before you open the explanation.

**Prefer a timed run?** The [practice test](https://preporato.github.io/claude-certification-guide/#ccao-f) has the same questions, scores every domain, and runs in your browser.

| Domain | Exam weight | Questions here |
|---|---|---|
| Output Evaluation and Validation | 21% | 6 |
| Workflow Integration and Solution Design | 16% | 5 |
| Governance, Risk, and Responsible Use | 15% | 5 |
| Prompting and Task Execution | 14% | 4 |
| Product and Model Selection | 12% | 4 |
| Configuration and Knowledge Management | 12% | 3 |
| Troubleshooting and Optimization | 10% | 3 |

---

### Question 1

*Output Evaluation and Validation*

Claude summarized a 30-page vendor contract you attached and wrote: 'The contract auto-renews for 24 months unless cancelled 90 days before expiry.' This line is going into an email to your director. What is the most efficient way to check it?

- **A.** Ask Claude to quote the exact clause and give its section number, then read that clause in the contract yourself
- **B.** Ask Claude whether it's sure
- **C.** Regenerate the summary and see whether the line comes back the same
- **D.** Send it as is, because the contract was attached

<details>
<summary>Answer</summary>

**A.** A grounded claim can point to its evidence, so asking for the clause and reading it yourself is fast and conclusive (A). Asking for reassurance (B) gets a fluent answer either way. Consistency across regenerations (C) doesn't prove accuracy. An attached source (D) lowers the risk of errors without removing it, and this line describes a contract commitment.

</details>

### Question 2

*Output Evaluation and Validation*

Claude drafted a job ad for a software engineer that uses phrases like 'young, energetic team' and 'digital native.' What is the issue, and what should you do?

- **A.** Nothing; these phrases are standard in job ads
- **B.** The wording signals an age preference, which can discourage qualified applicants and create legal risk; ask for inclusive wording and check it against your hiring policy
- **C.** The ad is too long; ask for a shorter version
- **D.** The tone is too casual for a job ad; ask for a formal rewrite

<details>
<summary>Answer</summary>

**B.** Evaluating output covers bias as well as factual errors, and age-coded language in a job ad is a real fairness and compliance problem (B). D and C change the style and keep the biased phrases. A confuses a common phrase with an acceptable one.

</details>

### Question 3

*Output Evaluation and Validation*

Claude built a pricing comparison table with totals calculated from 40 line items you pasted in. The table is going into a client proposal. What validation is needed?

- **A.** Round the totals so small differences don't matter
- **B.** Nothing, because you supplied the numbers
- **C.** Recompute the totals independently, for example in a spreadsheet, before the proposal goes out
- **D.** Ask Claude to double-check its math in the same chat

<details>
<summary>Answer</summary>

**C.** Precise arithmetic over many figures is a weak fit to accept unchecked, and a client-facing proposal makes the numbers consequential, so they get verified independently (C). The same process checking itself (D) isn't an independent check. Correct inputs (B) don't guarantee correct sums. Rounding (A) hides errors.

</details>

### Question 4

*Output Evaluation and Validation*

Claude wrote a market summary with no sources attached. Which TWO details are hallucination red flags? (Select TWO)

- **A.** 'According to a 2025 McKinsey survey, 73% of retailers plan to...' with no link or attached source
- **B.** A general explanation of what market share means
- **C.** A precise figure for next quarter's market size, stated as fact
- **D.** A note that Claude can't see your internal sales data
- **E.** A suggestion to verify the figures before publishing

<details>
<summary>Answer</summary>

**A and C.** A named study with a precise statistic and no source (A), and a confident, specific figure about the future (C), fit the red-flag profile: precision and authority without grounding. A general definition (B) is low risk, and E and D are signs of honest, calibrated output.

</details>

### Question 5

*Output Evaluation and Validation*

Claude summarized a customer interview and wrote: 'The customer is frustrated with onboarding and plans to cancel.' The transcript mentions onboarding friction but says nothing about cancelling. What is the problem?

- **A.** Nothing; it's a reasonable reading of the frustration
- **B.** The summary is too short
- **C.** The summary needs a more formal tone
- **D.** An unsupported inference is presented as fact; edit the line to what the transcript supports, or label it clearly as an interpretation

<details>
<summary>Answer</summary>

**D.** Details beyond the source are a hallucination red flag, and a cancellation claim could trigger real business decisions, so the output has to match its evidence (D). A plausible reading (A) still isn't supported by the transcript. B and C are style issues.

</details>

### Question 6

*Output Evaluation and Validation*

Research mode returns a summary of a new data regulation with eight cited sources. Your compliance team will base a plan on it. Which TWO steps are needed before anyone uses it? (Select TWO)

- **A.** Ask Claude to rate the reliability of each source
- **B.** Have the compliance owner review the conclusions before the plan is built on them
- **C.** Open the cited sources and confirm that each key claim matches what the source says, and that the sources are current and authoritative
- **D.** Run research mode again and keep the claims that appear twice
- **E.** Nothing; the citations prove the summary is accurate

<details>
<summary>Answer</summary>

**B and C.** Citations make claims checkable, which helps only if someone checks them (C), and regulatory content goes through a qualified reviewer (B). Citations alone (E) don't prove the summary represents its sources correctly. Repeated claims (D) show consistency, which isn't accuracy. Claude grading its own sources (A) is no independent check.

</details>

### Question 7

*Workflow Integration and Solution Design*

Your manager wants to roll Claude out to all 200 employees next week for every kind of task. What do you recommend?

- **A.** Let each employee figure it out without guidance
- **B.** Roll it out to everyone at once to build momentum
- **C.** Pilot one or two well-defined workflows with a small group, measure before and after (time spent, error rate), then expand
- **D.** Wait until AI tools stop making mistakes

<details>
<summary>Answer</summary>

**C.** A measured pilot shows the real value and the limits on a small scale before the whole company depends on it (C). A big-bang rollout (B) spreads untested habits everywhere at once. D waits for something that won't happen. A produces uneven quality and no evidence.

</details>

### Question 8

*Workflow Integration and Solution Design*

Which TWO tasks are strong fits for Claude in a marketing team's workflow? (Select TWO)

- **A.** Turning a webinar transcript into a blog draft and three social posts
- **B.** Deciding which agency gets a \$200,000 contract
- **C.** Reconciling 5,000 ad-spend transactions with no independent check
- **D.** Reporting a competitor's announcement from yesterday, from memory
- **E.** Drafting five subject-line variants for an A/B test

<details>
<summary>Answer</summary>

**A and E.** Drafting variants (E) and repurposing content across channels (A) are classic strong fits, with a person reviewing the output. A spending decision (B) needs human accountability, precise reconciliation at volume (C) belongs in a spreadsheet or finance system, and yesterday's news (D) is beyond the model's knowledge unless research mode grounds it.

</details>

### Question 9

*Workflow Integration and Solution Design*

You're presenting a Claude pilot to leadership. Which framing is most appropriate?

- **A.** 'Meeting summaries now take 10 minutes instead of 45. The meeting owner still reviews each one, because outputs can contain errors.'
- **B.** 'Claude eliminates errors from our summaries.'
- **C.** 'Claude will replace the operations team.'
- **D.** 'The benefits can't really be measured.'

<details>
<summary>Answer</summary>

**A.** Good stakeholder communication pairs a concrete, measured benefit with an honest limitation (A). B promises something no probabilistic system delivers. C overstates the role and invites resistance. D gives leadership nothing to decide with.

</details>

### Question 10

*Workflow Integration and Solution Design*

A colleague opens Claude and types 'help me with the Q3 board deck.' The results are unfocused. What should be defined before prompting?

- **A.** The slide color scheme
- **B.** Nothing; Claude should infer it
- **C.** Which model to use
- **D.** The deliverable, the audience, the source material and what a good result looks like

<details>
<summary>Answer</summary>

**D.** Solution design starts from the task: what you need, for whom, from which sources, and how you'll judge it (D). Model choice (C) comes later and won't rescue an undefined task. Claude can't infer goals nobody has stated (B). Colors (A) are a detail of the deliverable.

</details>

### Question 11

*Workflow Integration and Solution Design*

A legal team handles NDAs in five steps: intake, first-pass review against the team's playbook, negotiation, approval and signature. Where does Claude add the most value with the right safeguards?

- **A.** Signing on the company's behalf
- **B.** First-pass review: compare each NDA to the playbook and flag deviations for a lawyer to decide on
- **C.** Final approval
- **D.** Negotiating directly with the other party, unsupervised

<details>
<summary>Answer</summary>

**B.** Claude fits the draft-and-analyze stage, with a qualified person keeping the decision (B). Approval (C), signature (A) and unsupervised negotiation (D) would put legal accountability on a tool.

</details>

### Question 12

*Governance, Risk, and Responsible Use*

You want Claude to summarize an internal incident report that contains customers' names and email addresses. Your company's AI policy allows internal documents and prohibits customer personal data. What do you do?

- **A.** Paste it in and ask Claude to ignore the names
- **B.** Paste it in, because it's an internal document
- **C.** Use the most capable model so the data stays safe
- **D.** Remove or anonymize the customer details first (the summary doesn't need them), then summarize

<details>
<summary>Answer</summary>

**D.** Check the policy before pasting: the report is allowed, the customer data isn't, and the task works without it (D). Being internal (B) doesn't change the personal-data rule. Model choice (C) has nothing to do with data handling. Asking Claude to ignore data (A) comes after you've already shared it.

</details>

### Question 13

*Governance, Risk, and Responsible Use*

A sales rep wants to upload a prospect's RFP, marked confidential, so Claude can help draft the response. Your AI policy says nothing about third-party confidential documents. What is the best action?

- **A.** Ask the policy owner or legal before uploading, and treat the document as sensitive until there's an answer
- **B.** Upload only the pages that look less sensitive
- **C.** Upload it, since the policy doesn't forbid it
- **D.** Rewrite the RFP from memory and upload that

<details>
<summary>Answer</summary>

**A.** When the policy doesn't cover a case, escalate to the policy owner and stay on the cautious side in the meantime (A). Silence in the policy (C) doesn't amount to approval. Partial uploads (B) and paraphrasing from memory (D) still share confidential content, and the rewrite adds errors.

</details>

### Question 14

*Governance, Risk, and Responsible Use*

Your organization requires disclosure when AI helps produce external content. You drafted a customer newsletter with Claude and then edited it heavily. What applies?

- **A.** Disclose only if a customer asks
- **B.** Follow the disclosure rule as written, because your edits don't change how the draft was produced
- **C.** Describe the newsletter as written and fact-checked without AI
- **D.** Skip disclosure, because your edits make it your own work

<details>
<summary>Answer</summary>

**B.** Transparency rules apply as written (B). Editing (D) doesn't remove the requirement, disclosure on request (A) isn't what the policy says, and C misrepresents how the work was made.

</details>

### Question 15

*Governance, Risk, and Responsible Use*

Which TWO uses make Claude the decision-maker in a situation where a qualified person must own the call? (Select TWO)

- **A.** Brainstorming names for a team offsite
- **B.** Using Claude's ranking alone to decide which employees are laid off
- **C.** Drafting three versions of an internal FAQ for a manager to choose from
- **D.** Sending Claude's answer about a customer's legal rights to the customer without legal review
- **E.** Summarizing your own meeting notes

<details>
<summary>Answer</summary>

**B and D.** Decisions that affect people's livelihoods (B) or legal standing (D) need a qualified human to own them, however good the draft looks. C, A and E are drafting and organizing work where a person still chooses what to use.

</details>

### Question 16

*Governance, Risk, and Responsible Use*

A financial advisory firm uses Claude to draft client emails that explain investment options. Which control is essential?

- **A.** Using the most capable model
- **B.** A disclaimer at the bottom of every email, with no review
- **C.** Compliance review of client-facing investment content before it's sent, including a check of every figure
- **D.** Sending the drafts faster to improve service

<details>
<summary>Answer</summary>

**C.** Investment explanations are regulated advice, so qualified review comes before sending (C). A stronger model (A) doesn't change who is accountable. A disclaimer (B) can't replace the review that regulation requires. Speed (D) is beside the point.

</details>

### Question 17

*Prompting and Task Execution*

Your prompt 'Write an email about the new expense tool' produced something generic. Which TWO additions would improve it most? (Select TWO)

- **A.** The tool's key facts, attached or pasted in: launch date, how to get access, where to get help
- **B.** A switch to the most capable model
- **C.** A request for ten versions
- **D.** Who the email is for and what it should get them to do
- **E.** 'Make it amazing'

<details>
<summary>Answer</summary>

**A and D.** Generic output comes from missing context, and the audience and goal (D) and the source material (A) are two of the five parts of a complete business prompt. Enthusiasm (E) adds no information. More versions (C) of an underspecified email are more generic emails. A stronger model (B) still can't know facts you didn't give it.

</details>

### Question 18

*Prompting and Task Execution*

You need a 20-page market analysis with competitor profiles, a pricing comparison and recommendations. One big prompt produced a shallow result. What is the best approach?

- **A.** Rewrite the single prompt with every requirement in capitals
- **B.** Break it into steps: agree on an outline, draft each section from its sources, then do a final pass for consistency and tone
- **C.** Regenerate until a deeper version appears
- **D.** Ask for 'much more detail'

<details>
<summary>Answer</summary>

**B.** Multi-part deliverables work better as a sequence of smaller steps you can check (B). D and A keep the one-giant-prompt problem. C is regenerate-and-hope.

</details>

### Question 19

*Prompting and Task Execution*

Claude's first draft of a customer apology is too long and too formal. Which follow-up works best?

- **A.** Regenerate the response
- **B.** Start a new chat with the same prompt
- **C.** 'Cut this to about 120 words, make the tone warmer and more direct, keep the refund details, and apologize in the first sentence.'
- **D.** 'Make it better.'

<details>
<summary>Answer</summary>

**C.** Specific feedback gives Claude concrete changes to make (C). D gives it nothing to act on, and A and B roll the dice again on an unchanged request.

</details>

### Question 20

*Prompting and Task Execution*

You want campaign ideas for a product launch. Which prompting strategy fits brainstorming?

- **A.** Give no context, so Claude is unconstrained
- **B.** Ask for ideas with final budgets attached
- **C.** Ask for the single best idea
- **D.** Ask for many varied ideas first (say, 20 across different angles), then evaluate and narrow them with your criteria in a follow-up

<details>
<summary>Answer</summary>

**D.** Brainstorming works best as volume and variety first, then judgment (D). Asking for one best idea (C) skips the exploration. Budgets (B) belong to a later planning step. With no context (A), the ideas won't fit your product or audience.

</details>

### Question 21

*Product and Model Selection*

You need a project timeline that you'll revise with Claude over several rounds and then share with your team. Which output format fits?

- **A.** An Artifact: a standalone deliverable in its own panel that you can refine and share
- **B.** A screenshot of the chat
- **C.** Research mode
- **D.** A plain chat reply you copy out each time

<details>
<summary>Answer</summary>

**A.** Artifacts are made for standalone deliverables you'll iterate on and share (A). Chat replies (D) suit quick answers. Research mode (C) finds current sources. A screenshot (B) can't be edited.

</details>

### Question 22

*Product and Model Selection*

Which TWO tasks justify Opus over Sonnet? (Select TWO)

- **A.** Summarizing a short meeting
- **B.** A strategy recommendation that synthesizes six long reports, where an error would be expensive
- **C.** Writing a two-line reply to a colleague
- **D.** Working out how obligations interact across five related contracts before a high-stakes negotiation
- **E.** Reformatting a list of 30 names into a table

<details>
<summary>Answer</summary>

**B and D.** Opus is for complex, high-stakes reasoning across a lot of material (B, D). Sonnet is the everyday default, and quick, simple tasks like E, C and A suit Sonnet or Haiku.

</details>

### Question 23

*Product and Model Selection*

You need to sort 400 short customer comments into five well-defined themes today. Speed matters more than nuance. Which approach fits?

- **A.** Haiku with the five themes clearly defined, followed by a spot-check of a sample
- **B.** One comment per chat, so each gets full attention
- **C.** Opus for maximum quality on every comment
- **D.** Research mode

<details>
<summary>Answer</summary>

**A.** Quick, well-defined tasks at volume are Haiku's case, and a sample check keeps the quality honest (A). Opus (C) spends time and cost on a task that doesn't need deep reasoning. Research mode (D) searches for current sources, which this task doesn't need. B wastes hours.

</details>

### Question 24

*Product and Model Selection*

A long chat about a proposal has become slow, and Claude has started mixing up details from early drafts with the current version. What is the best move?

- **A.** Switch to Haiku for speed
- **B.** Paste the entire chat history into a new chat
- **C.** Start a new chat with a short summary of the current decisions and the latest draft, and keep reference documents in Project knowledge
- **D.** Keep going and correct each mistake as it appears

<details>
<summary>Answer</summary>

**C.** Restart, summarize and persist is the fix for an overloaded chat: a fresh context with only what matters (C). D keeps the overload, B moves it to a new chat, and A changes speed without fixing the mix-ups.

</details>

### Question 25

*Configuration and Knowledge Management*

In a team Project, where should each of these go: (1) 'Always write in British English and use our headline format'; (2) the 40-page brand guidelines PDF; (3) the brief for this week's campaign?

- **A.** (1) The chat prompt, (2) the chat prompt, (3) Project knowledge
- **B.** (1) Project instructions, (2) the chat prompt, (3) Project knowledge
- **C.** (1) Project knowledge, (2) Project instructions, (3) Project instructions
- **D.** (1) Project instructions, (2) Project knowledge, (3) the chat prompt

<details>
<summary>Answer</summary>

**D.** Standing rules go in instructions, reference documents go in knowledge, and details for one task go in the chat (D). C swaps rules and documents and makes a one-week brief permanent. A retypes standing rules every time. B re-uploads the guidelines in every chat and stores a temporary brief permanently.

</details>

### Question 26

*Configuration and Knowledge Management*

Your weekly report draws on a Google Doc of sales notes that the team updates daily. You've been uploading a copy every Monday, and sometimes it's out of date. What is the better setup?

- **A.** Copy the notes into the Project instructions
- **B.** Connect Google Drive so Claude reads the current version of the document
- **C.** Upload a copy twice a week
- **D.** Paste the notes from memory

<details>
<summary>Answer</summary>

**B.** Connectors suit material that lives in another tool and changes often, so Claude reads the current version (B). More frequent uploads (C) shrink the gap without closing it. Memory (D) adds errors. Instructions (A) hold standing rules, and pasted notes there go stale just as fast.

</details>

### Question 27

*Configuration and Knowledge Management*

A Project keeps quoting last year's prices. Both the 2025 and the 2026 price sheets are in Project knowledge. What fixes this?

- **A.** Remove or replace the outdated price sheet, and if both must stay, state in the instructions which one is current
- **B.** Use research mode for prices
- **C.** Correct Claude in every chat
- **D.** Switch to Opus

<details>
<summary>Answer</summary>

**A.** Stale knowledge produces confidently outdated answers, so the fix is maintaining the knowledge itself (A). Correcting every chat (C) never ends. A stronger model (D) still reads both sheets. Your prices are internal, so searching for them (B) won't find the right ones.

</details>

### Question 28

*Troubleshooting and Optimization*

You asked for 'a table comparing vendors,' and each time the columns come out different. What is the most effective fix?

- **A.** Ask for 'a better table'
- **B.** Show the exact structure: list the columns in order, or paste a sample row, and ask Claude to follow it
- **C.** Regenerate until the columns match
- **D.** Switch to Opus

<details>
<summary>Answer</summary>

**B.** A wrong format every time means the format was described vaguely, and a concrete example fixes that (B). C is regenerate-and-hope, D changes the model without clarifying the request, and A is still vague.

</details>

### Question 29

*Troubleshooting and Optimization*

Claude answered a question about your company's travel reimbursement limits using general industry norms. The real policy is a PDF on the shared drive. What is the best fix?

- **A.** Tell Claude its answer is wrong and ask it to try again
- **B.** Switch to Opus
- **C.** Attach the policy (or add it to Project knowledge) and ask Claude to answer from it, quoting the relevant section
- **D.** Ask the same question again with more emphasis

<details>
<summary>Answer</summary>

**C.** Confident but wrong claims about your own business come from missing source material, so give Claude the policy and ask for the quote (C). Emphasis (D) and a stronger model (B) can't produce a policy Claude hasn't seen. Telling Claude it's wrong (A) without the policy gets you a different guess.

</details>

### Question 30

*Troubleshooting and Optimization*

On Monday you changed a Project's instructions, switched the model and uploaded new knowledge files. Since then, the outputs are worse. What should you do?

- **A.** Change everything again
- **B.** Delete the Project and start over
- **C.** Ask Claude what went wrong
- **D.** Roll back, then reapply one change at a time and compare the results on the same test inputs

<details>
<summary>Answer</summary>

**D.** With three changes at once, you can't tell which one hurt quality, so change one variable at a time against the same inputs (D). A adds more confusion, C asks Claude to explain configuration changes it can't observe, and B throws away a setup that worked before Monday.

</details>

---

## Where to go next

- **Review by domain.** If your misses cluster, re-read those domains in Part II of the [CCAO-F study guide](./guide.md):
  - [Output Evaluation and Validation](./guide.md#domain-1-output-evaluation--validation-21)
  - [Workflow Integration and Solution Design](./guide.md#domain-2-workflow-integration--solution-design-16)
  - [Governance, Risk, and Responsible Use](./guide.md#domain-3-governance-risk--responsible-use-15)
  - [Prompting and Task Execution](./guide.md#domain-4-prompting--task-execution-14)
  - [Product and Model Selection](./guide.md#domain-5-product--model-selection-12)
  - [Configuration and Knowledge Management](./guide.md#domain-6-configuration--knowledge-management-12)
  - [Troubleshooting and Optimization](./guide.md#domain-7-troubleshooting--optimization-10)
- **Practice at full length.** The [CCAO-F page on Preporato](https://preporato.com/certificates/claude-certified-associate-foundations) has free sample questions and six full-length timed practice tests (paid) in the exam's format, with a score for every domain.

Found a mistake in a question? [Open an issue](https://github.com/preporato/claude-certification-guide/issues/new?template=outdated-fact.yml) and we'll fix it.

*These questions were written for this repo and are not taken from the exam. Not affiliated with Anthropic.*
