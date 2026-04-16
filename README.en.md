# IR Literature Review Skill

<p align="center">
  <strong>A Codex Skill for International Relations literature reviews</strong><br />
  It turns an outline and a search direction into a review organized around research tension, verified literature, and usable academic delivery.
</p>

<p align="center">
  <a href="./README.md">中文版</a> ·
  <a href="./SKILL.md">View SKILL.md</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Codex-Skill-111827?style=flat-square" alt="Codex Skill" />
  <img src="https://img.shields.io/badge/Language-Chinese%20first-0f766e?style=flat-square" alt="Chinese first" />
  <img src="https://img.shields.io/badge/Use-IR%20Literature%20Review-7c3aed?style=flat-square" alt="IR Literature Review" />
</p>

<p align="center">
  <sub>This repository is Chinese-first. English is available as an option.</sub>
</p>

## One-line Summary

`ir-literature-review` is a custom Claude Code skill for **International Relations literature review** tasks.

Its purpose is not to summarize a pile of papers, but to help an agent reliably do the things strong IR reviews require:

- identify the research question and tension first
- confirm the structure before drafting full text
- ground claims in verified literature
- produce a `.docx` file with academic formatting by default

## Good Fit

This skill is especially useful when:

- you already have a paper outline and need the review to match it
- you have a broad search direction and want a skeleton first
- you are writing on security studies, IPE, foreign policy analysis, international organizations, comparative authoritarianism, information politics, or constructivism
- you want the research gap to grow out of concrete limitations in existing work
- you need a deliverable that is ready to submit, not just plain text

It is **not primarily for**:

- generic essay-style background sections
- mechanical paper lists
- writing tasks that do not require a literature-review structure

## What the Skill Does

The default workflow is:

1. Extract the research question, mechanism, method scope, and competing literature.
2. Search and verify sources through Google Scholar or CNKI workflows.
3. Produce a literature-review skeleton and wait for confirmation.
4. Expand the confirmed skeleton into full prose.
5. Deliver citations, references, and a formatted `.docx` file.

By default it supports 3 output states:

| Output State | When to Use |
|---|---|
| `Skeleton draft` | the direction still needs confirmation |
| `Full review` | the question and structure are stable |
| `References + docx` | the user needs a ready-to-deliver draft |

## Retrieval Dependencies

This skill relies on two external skills during the literature-search phase:

- [gs-skills](https://github.com/cookjohn/gs-skills)
- [cnki-skills](https://github.com/cookjohn/cnki-skills)

They are used for English IR literature and Chinese IR literature search, verification, and follow-up reading.

## Default Writing Rules

| Rule | Meaning |
|---|---|
| Tension first | organize around disputes, mechanisms, and gaps, not paper-by-paper summaries |
| Structure first | confirm the argument structure before expansion |
| Verification first | unverified literature should not be treated as settled evidence |
| Delivery first | default output should be a usable `.docx` |
| Chinese first | the Chinese page and Chinese output are the default, English is optional |

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

## Repository Layout

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

- `SKILL.md`: main skill definition and execution protocol
- `EG1.txt`, `EG2.txt`: sample texts for different writing strategies
- `LR1.txt`, `LR2.txt`: literature-review method references
- `references/writing-strategies.md`: strategy detail reference
- `references/quality-checklist.md`: quality standards and common failure modes

## Quick Start

1. Open this repository in Claude Code.
2. Share your paper outline and search direction.
3. Confirm the skeleton before expanding the draft.
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

## Related Files

- Main skill file: [SKILL.md](./SKILL.md)
- Chinese homepage: [README.md](./README.md)
- Quality checklist: [references/quality-checklist.md](./references/quality-checklist.md)
- Writing strategies: [references/writing-strategies.md](./references/writing-strategies.md)

## Project Status

Actively maintained.

Current capabilities include:

- in-text citation and reference generation
- default `.docx` delivery
- automatic enforcement of academic formatting defaults
