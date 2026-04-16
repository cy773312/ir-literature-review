# ir-literature-review

[中文](./README.md) | English

<p align="left">
  <strong>A custom Claude Code skill for high-quality International Relations literature reviews.</strong>
</p>

<p align="left">
  It turns a paper outline and a literature-search direction into a review organized around research tension, backed by verified citations, and delivered in academic <code>.docx</code> format by default.
</p>

## Highlights

- **Tension-first writing**: focus on disputes, mechanisms, and gaps instead of paper-by-paper summaries.
- **IR-aware workflow**: supports security studies, IPE, foreign policy analysis, international organizations, comparative authoritarian politics, information politics, and constructivist research.
- **Verification-aware citations**: only cite checked sources; mark anything unverified explicitly.
- **Docx-first delivery**: final output is meant to be usable `.docx`, not plain text alone.
- **Chinese-first default**: English output is available when requested.

## What This Skill Does

When a user provides a paper outline and a literature-search direction, the skill usually:

1. Extracts the research question, mechanisms, method scope, and competing literature.
2. Searches and verifies relevant sources through Google Scholar or CNKI workflows.
3. Produces a literature-review skeleton and waits for confirmation.
4. Expands the confirmed skeleton into a full draft.
5. Delivers formatted text, references, and a `.docx` file.

## Default Output Contract

Unless the user specifies otherwise, the skill follows this contract:

| Item | Default |
|---|---|
| In-text citations | Author-year style |
| Reference list | Only works actually cited in the text |
| Chinese font | SimSun |
| Latin font / numbers | Times New Roman |
| Font size | 12pt |
| First-line indent | 2 Chinese characters |
| Line spacing | 1.5 |
| Final deliverable | `.docx` |

If a school or journal template is provided, that template takes priority.

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
- `EG1.txt`, `EG2.txt`: exemplar texts for different writing strategies.
- `LR1.txt`, `LR2.txt`: literature-review method references.
- `references/writing-strategies.md`: strategy detail reference.
- `references/quality-checklist.md`: quality standards and common failure modes.

## Quick Start

1. Open this repository in Claude Code.
2. Share the paper outline and broad literature-search direction.
3. Confirm the review skeleton before full drafting.
4. Generate the review with citations and references.
5. Export the final `.docx` file.

## Example Prompts

- “Based on my paper outline, draft an IR literature review. Give me the skeleton first.”
- “Use a question-driven strategy for deterrence failure mechanisms and compare competing explanations.”
- “Output in docx with SimSun for Chinese, Times New Roman for English/numbers, 12pt, first-line indent 2 characters, line spacing 1.5.”

## Design Principles

- A literature review is an argument, not a bibliography.
- Gaps should grow from limitations in existing studies.
- Critique should be sharp, grounded, and targeted.
- Transitions should follow logic, not filler phrasing.

## Contributing

Issues and pull requests are welcome.

Suggested improvements:

- expand IR subfield examples,
- improve citation and reference handling,
- strengthen multilingual retrieval and drafting workflows.

## Project Status

Actively maintained.

Current capabilities include:

- in-text citation and reference generation,
- default `.docx` delivery,
- automatic enforcement of academic formatting defaults.
