# IR Literature Review Tool

<p align="center">
  <strong>A tool for International Relations literature reviews</strong><br />
  Chinese-first, with English available as an option. Start from retrieval-based positioning, then build argument-driven prose with verified sources.
</p>

<p align="center">
  <a href="./README.md">中文版</a> ·
  <a href="./SKILL.md">View SKILL.md</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Home-Chinese%20first-0f766e?style=flat-square" alt="Chinese first" />
  <img src="https://img.shields.io/badge/English-optional-1d4ed8?style=flat-square" alt="English optional" />
  <img src="https://img.shields.io/badge/Retrieval-GS%20%2B%20CNKI-7c3aed?style=flat-square" alt="GS and CNKI" />
</p>

It prioritizes research tension and argument positioning over mechanical paper summaries, and supports:
- in-text citations grounded in verified sources,
- automatic reference list generation,
- `.docx` delivery with academic formatting defaults,
- **cross-user / cross-model consistency controls (fixed protocol + quality gates)**,
- **Chinese as the default output language, with optional English output on request**.

<p align="center">
  <sub>This repository is Chinese-first. English readers can start here.</sub>
</p>

## One-line Summary

`ir-literature-review` is a tool for **International Relations literature review** tasks.

`ir-literature-review` is built for workflows where users provide:
- at least a literature search scope,
- optionally a paper outline,
- and optional seed papers for retrieval expansion.

Execution flow:
1. Structure search boundaries, language/database priorities, inclusion criteria, and seed papers.
2. Retrieve and verify literature (Google Scholar / CNKI paths).
3. Output a “search scope + literature map” first and wait for confirmation.
4. Then move to research positioning and drafting (show skeleton first only when user asks).
5. Deliver final text with citations, references, and `.docx` output.

## Core Capabilities

- **Tension-first writing logic**: organize literature around theoretical/empirical tensions.
- **Two writing strategies**:
  - Framework integration (framework-first)
  - Question decomposition (question-driven)
- **IR subfield adaptation**: security studies, IPE, FPA, IOs, comparative authoritarian politics, constructivist/normative studies.
- **Citation integrity constraints**:
  - no fabricated references,
  - unverified details must be marked,
  - in-text citations must match the reference list.
- **Robustness controls**:
  - quality tiers (fast / standard / rigorous) for retrieval depth,
  - fixed "retrieval log + literature map" output protocol,
  - mandatory evidence/structure/positioning quality gates before drafting.
- **Docx-first delivery**: default output is a usable `.docx`, not plain text only.

## Default Output Contract

Unless the user specifies otherwise:

| Item | Default |
|---|---|
| In-text citations | Author-year style |
| Reference list | only works actually cited in the text |
| Chinese font | SimSun |
| Latin font / numbers | Times New Roman |
| Font size | 12pt |
| First-line indent | 2 Chinese characters |
| Line spacing | 1.5 |
| Final deliverable | `.docx` |

If a school or journal template is provided, that template takes priority.

## Quick Start

1. Open this repository in Claude Code.
2. Provide your literature search scope (optionally with outline + seed papers).
3. Confirm the generated “search scope + literature map” first.
4. Generate full text with citations and references (skeleton first only if needed).
5. Receive a `.docx` file with required formatting.

## Example Prompts

- “Start from this search scope and give me a literature map first: deterrence failure mechanisms, 2015–2025, English-first with Chinese supplements; I’ll also provide seed papers.”
- “Use my seed papers plus GS/CNKI retrieval, confirm coverage first, then draft a question-driven IR literature review.”
- “Output in docx with SimSun for Chinese, Times New Roman for English/numbers, 12pt, first-line indent 2 characters, line spacing 1.5.”

## Design Principles

- A literature review is an argument, not a bibliography.
- Gaps should grow from concrete limitations in existing studies.
- Critique must be sharp, grounded, and targeted.
- Transitions should follow argument logic, not connective filler.
- To keep quality close across users, agents, and models, prioritize fixed protocols and quality gates over free-form variation.

## Related Files

- Main instruction file: [SKILL.md](./SKILL.md)
- Chinese homepage: [README.md](./README.md)
- Quality checklist: [references/quality-checklist.md](./references/quality-checklist.md)
- Writing strategies: [references/writing-strategies.md](./references/writing-strategies.md)

## Project Status

Actively maintained.

Current capabilities include:

- in-text citation and reference generation
- default `.docx` delivery
- automatic enforcement of academic formatting defaults
