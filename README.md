<p align="center">
  <img src="assets/logo.png" alt="management-consulting" width="128">
</p>

# management-consulting — Strategy Skill for AI Coding Agents

A lightweight, open-source playbook for turning AI coding agents into structured strategy and decision partners.

This repository packages 42 practitioner-grade frameworks into reusable workflows for market analysis, competitive strategy, problem solving, pricing, operations, innovation, and decision-making. It is designed to help agents reason with structure, separate fact from inference, and produce output that is actionable instead of generic.

Built for Claude Code and compatible with Codex, Gemini CLI, Cursor, and any agent that reads SKILL.md files.

## Why this exists

Most AI outputs sound plausible but drift into generic framework-salad. This repo adds a disciplined process instead:

- **Clarify the decision first** — define the objective, decision, and constraints before analyzing.
- **Use the right framework for the real problem** — not every decision needs Five Forces or a SWOT deck.
- **Separate fact, inference, and assumption** — evidence quality matters as much as the answer.
- **Structure before hypothesis** — break the problem into decision-relevant questions and priority trade-offs.
- **Avoid shallow consultant-style answers** — check common failure modes, anti-patterns, and when a framework breaks down.

The package includes 42 frameworks, step-by-step application flows, concrete examples, and quality gates designed to keep AI reasoning useful in real business settings.

## Install

```bash
# Claude Code
cp -r management-consulting/ ~/.claude/skills/management-consulting/

# Or use npx
npx skills add gcamilo/management-consulting
```

## Usage

Just ask naturally. The skill activates on strategy questions, decisions, market analysis, due diligence, or structured recommendations.

**Quick Structure** — thinking out loud, exploratory
> "Help me think through build vs buy for our data pipeline"

**Full Case** — specific decision with real stakes
> "Should we expand into the mid-market segment?"

**Client Deliverable** — deck-ready, stakeholder-facing
> "Draft a strategy memo for the board on our market entry options"

## What's inside

```
management-consulting/
├── SKILL.md (258 lines)                    # Core: modes, workflow, output contract
├── references/
│   ├── frameworks-strategy.md (798 lines)  # Five Forces, Value Chain, 7S, VRIO, Blue Ocean...
│   ├── frameworks-financial.md (781 lines) # Profit Tree, Revenue Tree, TAM/SAM/SOM, Unit Econ
│   ├── frameworks-decision.md (708 lines)  # RAPID, Decision Matrix, Pre-Mortem, Inversion
│   ├── frameworks-pricing.md (688 lines)   # Value-Based, Cost-Plus, Competitive, Dynamic, Freemium
│   ├── frameworks-problem-solving.md (511) # MECE, Issue Tree, Hypothesis Tree, Pyramid
│   ├── frameworks-operations.md (484)      # ADKAR, Kotter, Lewin, Customer Journey, NPS
│   ├── frameworks-innovation.md (390)      # JTBD, Business Model Canvas, Advantage Matrix
│   ├── diagram-templates.md (231 lines)    # 12 diagram types (SVG templates)
│   ├── tooling-appendix.md (69 lines)      # Optional: rendering pipeline, themes
│   ├── frameworks-index.md (59 lines)      # Quick-reference: all 42 frameworks, one-line each
│   └── evidence-standards.md (24 lines)    # Claim labeling: Fact / Inference / Assumption / Estimate
├── examples/
│   ├── end-to-end-full-case.md (117)       # SaaS mid-market expansion (complete walkthrough)
│   ├── issue-tree-good-vs-bad.md (78)      # Before/after comparison
│   ├── recommendation-good-vs-bad.md (45)  # Before/after comparison
│   └── end-to-end-quick-structure.md (36)  # Build vs Buy (light mode)
└── variants/
    ├── strategy-memo.md (102)              # Pyramid Principle + SCQA + deck outline
    ├── due-diligence.md (81)               # Commercial DD + red flags
    ├── market-entry.md (80)                # Five Forces + TAM + positioning
    └── org-effectiveness.md (62)           # 7S + ADKAR + stakeholder mapping
```

**22 files. ~5,700 lines. ~333K chars.**

## Framework depth

Every framework reference file includes (per framework):

| Section | What it provides |
|---|---|
| **When to use** | The specific problem type this framework solves |
| **Step-by-step workflow** | Numbered practitioner steps — not theory, the actual work |
| **Good vs bad output** | Concrete examples with real numbers showing shallow vs actionable |
| **Common mistakes** | 3-5 things practitioners get wrong, with root cause |
| **When it breaks down** | Failure conditions — when the framework misleads |
| **Best combinations** | Which frameworks pair well, in what sequence |

### 42 frameworks across 7 categories

> **[Visual Reference Guide](https://gcamilo.github.io/management-consulting/)** — interactive cards with diagrams, examples, step-by-step mechanics, and key questions for each framework.

**[Strategy (11)](https://gcamilo.github.io/management-consulting/#strategy):** Five Forces, Value Chain, 7S, VRIO, 3 Horizons, Ansoff, Growth-Share Matrix, Nine-Box, Blue Ocean, Wardley Mapping, Scenario Planning

**[Problem Solving (6)](https://gcamilo.github.io/management-consulting/#problem-solving):** MECE, Issue Trees, Hypothesis Trees, 7-Step Problem Solving, Pyramid Principle, SCQA

**[Decision Making (5)](https://gcamilo.github.io/management-consulting/#decision-making):** RAPID, Decision Matrix, Pre-Mortem, Second-Order Thinking, Inversion

**[Financial (5)](https://gcamilo.github.io/management-consulting/#financial):** Profit Tree, Revenue Tree, TAM/SAM/SOM, Unit Economics, Waterfall/Bridge

**[Operations (6)](https://gcamilo.github.io/management-consulting/#operations):** ADKAR, Kotter's 8-Step, Lewin's Change Model, Influence Model, Customer Journey, NPS

**[Innovation (4)](https://gcamilo.github.io/management-consulting/#innovation):** Jobs to Be Done, Business Model Canvas, Value Proposition Canvas, Advantage Matrix

**[Pricing (5)](https://gcamilo.github.io/management-consulting/#pricing):** Value-Based, Cost-Plus, Competitive, Dynamic, Freemium

## How it was built

1. **3-way AI research** — Gemini, Codex, and Claude independently researched all 42 frameworks in parallel (21 research tasks, 497K chars of raw material)
2. **Synthesis** — 4 agents merged the best from each AI per category. Took the sharpest examples, cut textbook filler, resolved disagreements.
3. **3 rounds of adversarial review** — Codex (scored 7/10), Gemini (scored 9.4/10), and self-review identified gaps in portability, completeness, and actionability. All addressed.
4. **A/B eval** — 7-way comparison of different reference configurations to find the highest-impact bundle.
5. **v2 eval redesign** — 9-criteria rubric with programmatic checkers, pairwise comparison with position swap, and Gemini+Codex adversarial review of the eval plan itself. Key finding: baseline beating the skill on some prompts revealed a skill bug (hard gate too aggressive — the skill stopped at clarifying questions on vague prompts instead of stating assumptions and proceeding), not a measurement problem. But the rubric redesign was needed to properly measure process discipline, which the v1 absolute scoring missed.

## Eval results

### Latest: Post-polish (Apr 29 2026) — [skill-eval](https://github.com/gcamilo/skill-eval) v2 rubric

Re-run after the Apr 29 polish (mode-detection cues, `KILL CONDITIONS` section, `[E]` evidence label, context-check rename). Gemini-flash judge, Sonnet generation, `skill_only` approach (no examples bundle).

**Skill wins 3/3 prompts:**

| Prompt | Tier | Skill | Baseline | Δ |
|---|---|---|---|---|
| market-entry | standard | **9.7** | 7.5 | +2.2 |
| ambig-competitive | ambiguous | **6.8** | 5.5 | +1.3 |
| adv-framework-salad | adversarial | **6.8** | 6.0 | +0.8 |
| **Average** | — | **7.8** | **6.3** | **+1.5** |

**By tier:**

| Tier | What it measures | Skill | Baseline | Δ |
|------|-----------------|-------|----------|---|
| T1 — Process Discipline | Structure, framing, evidence | **6.1** | 3.9 | **+2.2** |
| T2 — Output Quality | Specificity, insights, formatting | 7.6 | 7.1 | +0.5 |
| T3 — Decision Quality | Options, falsifiability, assumptions | **9.7** | 8.0 | **+1.7** |

![Eval Results](assets/eval-results.png)

The hard prompts show the polished skill correctly applying **Quick Structure mode** — shorter, focused responses that ask for the data needed before going deeper. On the framework-salad adversarial prompt, Decision Quality scored 10.0 (judge agreed that pushing back on the 4-framework request was the right call), even though Process Discipline scored lower because the response was short. The rubric still rewards heavy structure; the skill now correctly trades structure for responsiveness on vague/adversarial inputs.

### Pre-polish baseline (Apr 24 2026)

#### Anthropic skill-creator blind A/B (`/skill-creator`, Opus judge)

| Prompt type | Skill | Baseline |
|---|---|---|
| Market entry | 9.5 | 7.0 |
| Competitive threat | 9.0 | 5.5 |
| Framework salad | 9.0 | 7.0 |
| **Average** | **9.2** | **6.5** |

The judge identified **process discipline** as the key differentiator — the skill enforces structured framing and evidence labeling that the baseline skips. Not yet re-run after the Apr 29 polish.

#### Custom dual-judge eval (skill-eval v2, Gemini 3.1 Pro + Claude Sonnet)

| Tier | Skill delta |
|------|-------------|
| T1 — Process Discipline | +1.6 |
| T2 — Output Quality | +0.6 |
| T3 — Decision Quality | +0.4 |

Notable findings:
- **Easy prompts show the largest T1 gap** (+4.8) — the skill enforces structure that the model naturally skips on simple questions
- **Evidence labeling is the sharpest signal** — 48–99 labeled claims per response vs 0 baseline; no overlap between distributions

## Customization

- **Add variants** — `variants/your-scenario.md` with upfront questions, required frameworks, deliverables
- **Add examples** — `examples/your-example.md` showing input → mode → output
- **Adjust strictness** — edit hard gate, output contract, or quality checklist in SKILL.md
- **Add frameworks** — create or extend `references/frameworks-{category}.md`

## License

MIT
