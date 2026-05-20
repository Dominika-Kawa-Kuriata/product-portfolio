# Job Search Co-Pilot

A custom Claude Project that acts as a structured sparring partner for job search. Built during the 10x Product Bootcamp (Product Academy, April–May 2026) as a practical exercise in AI-augmented personal workflow design.

## The problem

Job searching as a senior Product Owner involves repetitive cognitive overhead: parsing offers, calibrating salary anchors, drafting tailored applications, researching companies before interviews. Generic AI assistants help with isolated tasks but lose context across sessions, encourage embellishment, plus produce buzzword-heavy outputs that read as generic.

I wanted a tool that knew my CV, my case study bank, my claim boundaries plus my market anchors, so every session would be calibrated rather than generic.

## What I built

A system prompt with four operating modes:

**Mode 1 — Job Fit Filter.** Paste a job offer, get a structured 5-line output: fit score 1-10, salary expectations, red flags, green flags, go/no-go decision. Hard rule: if fit is below 5, no deep analysis, just one sentence why not.

**Mode 2 — Company Research Brief.** Give a company name, get a structured one-page brief covering what they do, scale, values with concrete quotes, recent news, product maturity assessment, positioning angles plus sharp questions to ask in interview.

**Mode 3 — Application Form Drafting.** Workflow that checks the case study bank first, calibrates tone for company stage (scaleup vs enterprise), produces drafts with a short “what I changed and why” rationale.

**Mode 4 — Interview Simulation.** Voice-mode practice with realistic recruiter behaviour, short feedback after each answer on three axes: content, structure (STAR for behavioural), communication.

Each session ends with a tab-separated row ready to paste into a Google Sheets tracker that captures application metadata plus time saved versus doing it without AI.

## Design decisions worth flagging

**Claim boundaries as a first-class section.** The system prompt has an explicit “never claim this” list: AI products as owned product when I only use AI in workflow, senior UX designer when I have UI collaboration support, domain expertise in fields I don’t know. This shapes every draft. Without it, the assistant naturally drifts toward exaggeration.

**Language conventions baked in.** British English spelling, no Oxford comma, no em-dashes, no buzzwords without backing, target lengths 150 / 250 / 350 words. Defined once at the top so I don’t repeat myself across sessions.

**A case study bank rather than improvisation.** Three named cases from my actual work, each tagged with the question types they fit. The assistant references these instead of inventing examples. If a question doesn’t match a banked case, it asks me for the real situation rather than making one up.

**Anchor a single number, not a range.** For each offer, the assistant suggests a concrete salary anchor with reasoning, calibrated to maximise win probability rather than maximum amount. The constitution is explicit: a 5% lower anchor that closes the deal beats a maximum anchor that kills it.

## What I learned

Building this taught me more about prompt engineering than any tutorial. The biggest insight was that **the constraints sections do more work than the instructions sections**. Telling the assistant what NOT to do, what NOT to claim, what tone NOT to use, produced sharper outputs than adding more positive instructions.

Second insight: structured outputs with explicit token budgets (150 / 250 / 350 word targets) made the assistant respect length on first try, rather than over-producing then needing trimming.

Third: a clear escalation path matters. Mode 1 ends with an offer to move to Mode 2 or 3 only if fit is 7+. This stopped the assistant from auto-deepening into companies that weren’t worth my time.

## Template

I anonymised the system prompt so others can adapt it for their own job search. The template keeps the full structure plus my examples in italics as patterns to follow:

→ [job-search-copilot-template.md](./assets/job-search-copilot-template.md)

Built and tested over six weeks of active job search. Early tracker data suggests meaningful time reduction on application drafting plus company research compared to doing it manually, with the bigger win being consistency: every output calibrated to the same standards rather than drifting session by session.
