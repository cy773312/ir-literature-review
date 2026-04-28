# IR Literature Review

<p align="center">
  <strong>Write IR literature reviews at top-journal quality with AI</strong><br />
  <sub>From your existing literature to argument-driven prose · Auto-citation · One-click docx</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/discipline-IR%20%7C%20International%20Relations-0f766e?style=flat-square" alt="IR" />
  <img src="https://img.shields.io/badge/output-docx-1d4ed8?style=flat-square" alt="docx" />
  <img src="https://img.shields.io/badge/language-中文%20%7C%20English-7c3aed?style=flat-square" alt="bilingual" />
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="license" />
</p>

<p align="center">
  <a href="./README.md">中文版</a> ·
  <a href="./SKILL.md">SKILL.md</a> ·
  <a href="#quick-start">Quick Start</a> ·
  <a href="#design-philosophy">Philosophy</a>
</p>

---

## What Is This

**IR Literature Review** is a Claude Code Skill that transforms your existing IR literature into high-quality literature reviews.

You bring the research topic and your literature (abstracts, PDFs, notes, bibliographies). It handles:

- Functional classification and close reading of each source
- Identification of core research tensions and optimal writing strategy
- Argument-driven prose — not mechanical summaries
- Automatic in-text citations and reference lists
- One-click `.docx` output with academic formatting

> This is not a literature search tool. For retrieval, pair with [gs-skills](https://github.com/cookjohn/gs-skills) or [cnki-skills](https://github.com/cookjohn/cnki-skills).

## Core Philosophy

<p align="center">
  <strong>The unit of analysis is not the paper — it's the problem and the tension.</strong>
</p>

A good IR literature review reads like an argument, not a catalog. It uses existing research to surface a structural tension and position new research within it.

## Capabilities

- **Tension-first writing** — organize around theoretical dilemmas, empirical debates, conceptual ambiguity, or methodological gaps
- **Two writing strategies** — Framework Integration or Question Decomposition, mixable
- **Gap typology** — consensus-zone gaps, debate-zone gaps, blank-zone gaps, each with distinct treatment
- **Four-dimension evaluation** — assumptions / logic / evidence / methodology, adapted from Knopf (2006)
- **10 evaluation methods** — from Wang & Tang (2022) for explanatory IR research
- **Citation integrity** — no fabricated references; all citations traceable to user-provided materials
- **Quality gates** — citation gate, structure gate, positioning gate
- **Automatic docx delivery** — SimSun / Times New Roman, 12pt, 1.5× line spacing, first-line indent
- **IR subfield coverage** — security studies, IPE, FPA, international institutions, comparative authoritarian politics, constructivism

## Quick Start

1. Open this repository in Claude Code
2. Provide your research topic + existing literature materials
3. The Skill builds a literature map, then writes upon confirmation
4. Receive a `.docx` with full citations and references

**Example prompts**:

```
I'm writing a review on "how digital authoritarianism shapes transnational
political mobilization." Key sources: Rosenfeld & Wallace (2024), Guriev &
Treisman (2022), Roberts (2018). Classify and evaluate these first, then
write using the question-driven strategy.
```

```
I have outlines and abstracts for papers on alliance credibility. Help me
build a literature inventory — identify core debates and gaps — before we
move to full drafting.
```

## Methodology Foundation

This Skill's writing methodology is distilled from four reference works:

| Source | Contribution |
|---|---|
| **Knopf (2006)** *Doing a Literature Review* | Four-task framework, four-dimension evaluation, two-tier literature structure, contribution framing |
| **Wang & Tang (2022)** Ch. 3 "How to Evaluate Literature" | Legitimacy/feasibility framework, 10 explanatory evaluation methods, four quality criteria, common errors |
| **Clark, Dolan & Jost (2025)** *Bureaucratic Influence in International Politics* | Framework-First strategy demonstration |
| **Rosenfeld & Wallace** *Information Politics and Propaganda in Authoritarian Societies* | Question-Driven strategy demonstration |

## Design Philosophy

- A literature review is an **argument**, not a bibliography
- Gaps must **grow** from concrete limitations in existing studies
- Critique must be **sharp, grounded, and targeted**
- Transitions follow **logical momentum**, not filler phrases
- Every gap must answer: **where does it come from?** and **what follows if unfilled?**
- Quality gates raise the **floor** — the ceiling is unlimited

## Output Defaults

| Item | Default |
|---|---|
| In-text citations | Author-year |
| Reference list | Only works actually cited |
| Chinese font | SimSun |
| Latin / numerals | Times New Roman |
| Font size | 12pt |
| First-line indent | 2 Chinese characters |
| Line spacing | 1.5× |
| Deliverable | `.docx` |

If you provide a school or journal template, it overrides these defaults.

## Repository Files

| File | Description |
|---|---|
| [SKILL.md](./SKILL.md) | Complete Skill instructions |
| [README.md](./README.md) | 中文主页 |
| [references/quality-checklist.md](./references/quality-checklist.md) | Literature evaluation quality checklist |
| [references/writing-strategies.md](./references/writing-strategies.md) | Detailed writing strategies |

---

<p align="center">
  <strong>🤝 Join Us in Building an Open-Source Ecosystem for IR × AI</strong>
</p>

International Relations research stands at a pivotal moment for AI empowerment. Literature reviews are just the beginning — fact retrieval, causal inference assistance, policy scenario simulation, multilingual intelligence analysis — every link in the IR research chain holds enormous potential for tooling.

But this ecosystem cannot be built by a handful of people. **IR scholars know what their research needs. Engineers know how to build it. Only when these two communities engage in sustained open-source dialogue can we create tools that truly work.**

If you:

- Used this Skill to write a literature review — share your experience and suggestions
- Have an idea for another IR research task that could benefit from AI — open an Issue or submit a PR
- Built your own IR-related Claude Code Skill — let us know so we can cross-link
- Just passing by and find this interesting — a ⭐ Star goes a long way

<p align="center">
  <strong>AI-powered IR research needs every one of you.</strong>
</p>

---

<p align="center">
  <sub>MIT License · Actively maintained</sub>
</p>
