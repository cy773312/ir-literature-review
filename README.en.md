# ir-literature-review

[中文](./README.md) | [English](./README.en.md)

A custom **Claude Code skill** for producing high-quality literature reviews in International Relations (IR).

It prioritizes research tension and argument positioning over mechanical paper summaries, and supports:
- in-text citations grounded in verified sources,
- automatic reference list generation,
- `.docx` delivery with academic formatting defaults,
- **Chinese as the default output language, with optional English output on request**.

## Table of Contents

- [Overview](#overview)
- [Core Capabilities](#core-capabilities)
- [Default Output Contract](#default-output-contract)
- [Repository Structure](#repository-structure)
- [Quick Start](#quick-start)
- [Example Prompts](#example-prompts)
- [Design Principles](#design-principles)
- [Contributing](#contributing)
- [Project Status](#project-status)

## Overview

`ir-literature-review` is built for workflows where users provide:
- a paper outline,
- a broad literature-search direction,
- and optionally known competing studies.

Execution flow:
1. Structure the research question, mechanisms, method scope, and competing literature.
2. Retrieve and verify literature (Google Scholar / CNKI paths).
3. Output a review skeleton and wait for user confirmation.
4. Expand into full draft using the selected writing strategy.
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
- **Docx-first delivery**: default output is a usable `.docx`, not plain text only.

## Default Output Contract

Unless the user specifies otherwise, the default is:

- **In-text citations**: author-year style (e.g., `Rosenfeld & Wallace, 2024`)
- **Reference list**: includes only works actually cited in the text
- **Document formatting**:
  - Chinese font: SimSun
  - Latin letters & numbers: Times New Roman
  - Font size: 12pt
  - First-line indent: 2 characters
  - Line spacing: 1.5

If a school/journal template is provided, template rules override defaults.

## Repository Structure

```text
.
├── SKILL.md
├── EG1.txt
├── EG2.txt
├── LR1.txt
├── LR2.txt
└── references/
    ├── writing-strategies.md
    └── quality-checklist.md
```

- `SKILL.md`: main skill definition and execution protocol.
- `EG1.txt`, `EG2.txt`: high-quality IR exemplar texts for different writing strategies.
- `LR1.txt`, `LR2.txt`: method references for literature review practice.
- `references/writing-strategies.md`: detailed strategy expansion.
- `references/quality-checklist.md`: quality dimensions and common failure modes.

## Quick Start

1. Open this repository in Claude Code.
2. Provide your paper outline and literature-search direction.
3. Confirm the generated review skeleton first.
4. Generate full text with citations and references.
5. Receive a `.docx` file with required formatting.

## Example Prompts

- “Based on my paper outline, draft an IR literature review. Give me the skeleton first.”
- “Use a question-driven strategy for deterrence failure mechanisms and compare competing explanations.”
- “Output in docx with SimSun for Chinese, Times New Roman for English/numbers, 12pt, first-line indent 2 characters, line spacing 1.5.”

## Design Principles

- A literature review is an argument, not a bibliography.
- Gaps should grow from concrete limitations in existing studies.
- Critique must be sharp, grounded, and targeted.
- Transitions should follow argument logic, not connective filler.

## Contributing

Issues and PRs are welcome.

Suggested directions:
- add more IR subfield exemplars,
- improve citation/reference adapters,
- strengthen multilingual retrieval and drafting workflows.

## Project Status

Actively maintained.

Current version supports:
- in-text citation and reference generation,
- default `.docx` delivery,
- automatic enforcement of academic formatting defaults.