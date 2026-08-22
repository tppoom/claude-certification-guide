# CCDV-F: Claude Certified Developer - Foundations

The developer credential. CCDV-F validates that an engineer can build real applications on the Claude platform: calling the API correctly, selecting models deliberately, constructing agents, wiring in tools, and shipping systems that are secure and testable.

## Quick facts

| | |
|---|---|
| Price | $125 per attempt |
| Questions | 53 (all scored) |
| Duration | 120 minutes |
| Passing score | 720 on a 100-1000 scaled score |
| Delivery | Pearson VUE, test center or online proctored |
| Validity | 1 year, free renewal assessment before expiration |
| Recommended experience | 1-5 years software engineering, 6+ months hands-on Claude or LLM work, fluency in Python or TypeScript, REST APIs, command line |

## Exam domains

| Domain | Weight |
|--------|--------|
| Applications and Integration | 33% |
| Model Selection and Optimization | 17% |
| Agents and Workflows | 15% |
| Prompt and Context Engineering | 11% |
| Tools and MCPs | 10% |
| Security and Safety | 8% |
| Claude Code | 3% |
| Eval, Testing, and Debugging | 3% |

The blueprint is implementation-heavy. The dominant domain, Applications and Integration at 33%, covers API mechanics: messages, streaming, vision, extended thinking, prompt caching, and batch processing, plus application lifecycle and configuration management. Agents are built with the Claude Agent SDK; tools connect through the Model Context Protocol (MCP), the open protocol that standardizes how models discover and call external tools and data sources.

**Note the question count: 53 is the smallest in the program.** Each miss costs slightly more, which rewards even coverage across the blueprint over deep expertise in one domain.

## Study path (~4 weeks part-time)

1. **Week 1: official baseline.** Join the [Claude Partner Network](https://claude.com/partners) (free), complete the Partner Academy developer courses, and read the exam guide.
2. **Weeks 2-3: build against the API.** Work through [docs.anthropic.com](https://docs.anthropic.com) with code open: streaming, prompt caching, batch processing, an agent with the Agent SDK, at least one MCP integration. The 33% integration domain is won in an editor, and the model-selection domain rewards actually comparing cost and latency across model tiers.
3. **Week 4: calibrate.** Full-length timed practice tests, then per-domain review. With 53 questions, a weak 10% domain is the difference between passing and retaking.

## Common mistakes

- Skipping the small domains. Security (8%), Claude Code (3%), and eval/debugging (3%) look ignorable, but together they are a seventh of a short exam.
- Knowing the API but not the economics. Model selection and cost optimization is the second-largest domain, and it expects deliberate reasoning about tiers, caching, and batching, plus when each is the wrong tool.
- Letting the credential lapse: renewal is free before the 12-month mark and a full-price proctored retake after it.

## Resources

**Official (free):**
- [Anthropic Partner Academy](https://claude.com/partners): courses and exam registration
- [docs.anthropic.com](https://docs.anthropic.com): API reference, Agent SDK, MCP

**Free deep-dives:**
- [CCDV-F complete guide](https://preporato.com/blog/claude-certified-developer-foundations-complete-guide-2026)
- [4-week study plan](https://preporato.com/blog/ccdv-f-study-plan-4-week-preparation-2026)
- [CCDV-F vs CCA-F: which to take](https://preporato.com/blog/ccdv-f-vs-cca-f-which-claude-certification-2026)

**Practice ([preporato.com/certificates/claude-certified-developer-foundations](https://preporato.com/certificates/claude-certified-developer-foundations)):**
- Free sample questions on the certification page
- (Paid) Six full-length 53-question practice tests and a 500-card flashcard deck built on the exact domain weights
- (Paid) 21 hands-on projects: build-and-submit work (API integration, agents, tools, extraction pipelines) graded automatically against a rubric
