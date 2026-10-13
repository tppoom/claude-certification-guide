# CCAR-P: Claude Certified Architect - Professional

> **[📖 The Complete CCAR-P Study Guide](./guide.md)**: the full preparation guide with 8 chapters, per-domain exam notes, worked questions, the nine trap answers, and exam-day strategy. This page is the summary; the guide is the study material.
>
> **Practice:** [30 practice questions](./practice-questions.md) · [Timed practice test](https://preporato.github.io/claude-certification-guide/#ccar-p) · [Full CCAR-P practice tests on Preporato](https://preporato.com/certificates/claude-certified-architect-professional)
>
> **Download:** [PDF](../downloads/ccar-p-study-guide.pdf) · [EPUB](../downloads/ccar-p-study-guide.epub), with the practice questions included
>
> **At a glance:** 8 chapters · 7 code examples · 12 worked questions · 30 practice questions · ~7,100 words

The top tier of the Anthropic certification program and its only Professional-level credential. CCAR-P certifies the person accountable for a Claude solution across its whole life: translating a vague business request into an architecture, selecting integration mechanisms, designing evaluation and governance into the system from day one, managing stakeholder expectations, and enabling the teams who build and operate the result.

## Quick facts

| | |
|---|---|
| Price | $175 per attempt (the most expensive in the program) |
| Questions | 63 (all scored, the longest exam in the program) |
| Duration | 120 minutes to answer, about 135 minutes of seat time |
| Passing score | 720 on a 100-1000 scaled score |
| Delivery | Pearson VUE, test center or online proctored |
| Languages | English or Japanese |
| Who can register | People who work at Claude Partner Network organizations, with a company email |
| Validity | 1 year, free renewal assessment before expiration |
| Prerequisites | None formally; CCA-F is optional but most candidates benefit from the Foundations vocabulary first |
| Recommended experience | 3+ years systems architecture or platform engineering, 6+ months delivering production Claude or LLM solutions |

## Exam domains

| Domain | Weight |
|--------|--------|
| Integration | 19% |
| Solution Design & Architecture | 17% |
| Evaluation, Testing & Optimization | 16% |
| Governance, Safety & Risk Management | 14% |
| Stakeholder Communication & Lifecycle Management | 14% |
| Claude Models, Prompting & Context Engineering | 13% |
| Developer Productivity & Operational Enablement | 7% |

## What the exam actually tests

The blueprint reads like an enterprise engagement:

- **Integration (the largest domain)**: MCP versus direct API versus agent-to-agent connections, retrieval-augmented generation (RAG) pipeline design, and security gaps in tool configurations.
- **Governance**: guardrails, human-in-the-loop placement, and compliance regimes such as GDPR and HIPAA.
- **The stakeholder domain is the one that surprises people.** A full 14% tests discovery, expectation setting, documentation, and feedback loops. Technically strong candidates lose more points here than anywhere else, because nothing in a developer's day-to-day prepares them for questions about running a discovery workshop or handling an executive's shifting success criteria.

The scenario questions demand judgment that is hard to cram. This is deliberate: the exam certifies solution ownership rather than implementation skill, which the Foundations tier already covers.

## Study path (~6 weeks part-time)

1. **Weeks 1-2: official baseline plus gap map.** Check that your employer is in the [Claude Partner Network](https://claude.com/partners) (registration needs your company email), complete the Partner Academy architect courses, read the exam guide, and honestly map your experience against all seven domains. Most candidates find their gap is in governance or stakeholder work rather than technology.
2. **Weeks 3-4: deepen the enterprise domains.** Work through [docs.anthropic.com](https://docs.anthropic.com) on integration patterns, evaluation design, and guardrails, and study how compliance regimes map onto LLM systems. If you have never run discovery or written an architecture decision record for a real stakeholder, practice on a hypothetical engagement end to end.
3. **Weeks 5-6: calibrate.** Full-length, timed 63-question practice tests. Use the per-domain breakdown ruthlessly; with seven domains, a comfortable overall average can hide a failing stakeholder or governance score.

## Common mistakes

- Preparing as if it were a harder CCA-F. The Professional exam spends most of its questions above the code, at the architecture, evaluation, governance, and communication level.
- Ignoring the two "soft" domains. Stakeholder communication plus lifecycle management is 14%, roughly nine questions, and they are the most commonly failed.
- Skipping evaluation design. Sixteen percent of the exam expects you to design eval datasets, metrics, and testing strategy into a solution from the start.
- Letting the credential lapse: renewal is free before the 12-month mark and a full-price proctored retake after it.
- Booking a retake on impulse: every attempt costs the full fee, and the wait grows from 14 to 30 to 90 days after each failed attempt.

## Resources

**Official (free):**
- [Anthropic Partner Academy](https://claude.com/partners): courses and exam registration
- [docs.anthropic.com](https://docs.anthropic.com): integration, agents, guardrails

**Free articles:**
- [CCAR-P complete guide](https://preporato.com/blog/claude-certified-architect-professional-complete-guide-2026)
- [6-week study plan](https://preporato.com/blog/ccar-p-study-plan-6-week-preparation-2026)
- [CCA-F vs CCAR-P: which to take](https://preporato.com/blog/cca-f-vs-ccar-p-which-claude-certification-2026)
- [Exam domains: complete breakdown](https://preporato.com/blog/ccar-p-exam-domains-complete-breakdown-2026)

**Practice:**
- [30 practice questions with explanations](./practice-questions.md) in this repo, also as a timed [practice test](https://preporato.github.io/claude-certification-guide/#ccar-p) (free)
- [The CCAR-P page on Preporato](https://preporato.com/certificates/claude-certified-architect-professional): free sample questions to start, then the full tests below
- (Paid) [Six full-length 63-question practice tests and a 500-card flashcard deck](https://preporato.com/certificates/claude-certified-architect-professional) built on the exact domain weights
- (Paid) [18 hands-on projects](https://preporato.com/certificates/claude-certified-architect-professional): build-and-submit work at the architecture level graded automatically against a rubric
