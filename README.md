<div align="center">
    <h1>Awesome Claude Code / Codex — Paper Proofreading</h1>
    <a href="https://github.com/LimHyungTae/awesome-claudecode-paper-proofreading"><img src="https://img.shields.io/badge/Claude_Code_+_Codex-Dual_Compatible-2b6cb0" /></a>
    <br />
    <br />
    <p align="center"><img src="https://github.com/user-attachments/assets/b2a97cb8-8535-4beb-b6af-2f641d1962c9" alt="Demo" width="95%"/></p>
    <p><strong><em>Detect first. Fix with confidence.</em></strong></p>
</div>

______________________________________________________________________

## :rocket: Overview

This repository is designed to work with **both Claude Code and Codex** while preserving the original proofreading philosophy.

The detailed instructions live in the `prompts/` folder. You can use them directly in a session, or copy/merge them into Codex-oriented workspace instructions such as `AGENTS.md`. For PhD theses in robotics, use [`prompts/04_thesis_proofreading.md`](prompts/04_thesis_proofreading.md).

The workflow remains **two-phase**: the agent detects and lists all issues with unique numbers `[1]`, `[2]`, `[3]`..., then waits. The user selects which issues to fix or discard before any file is modified.

______________________________________________________________________

## :bust_in_silhouette: About the Author

<p align="center"><img src="https://github.com/user-attachments/assets/4af4b29f-ce85-47a0-9472-406f2ca95572" alt="Hyungtae Lim" width="75%"/></p>

These prompts are distilled from years of hands-on paper reviewing and mentoring experience by **[Hyungtae Lim](https://github.com/LimHyungTae)**, a researcher in robotics and 3D perception.

- 📝 **[Associate Editor](https://www.ieee-ras.org/publications/ra-l/editorial-board/)**, IEEE Robotics and Automation Letters (RA-L)
- 🌟 **[RSS Pioneer 2024](https://sites.google.com/view/rsspioneers2024/participants)**
- 🎖️ **[ICRA 2025 Outstanding Reviewer](https://2025.ieee-icra.org/program/awards-and-finalists/#outstandingreviewer)** — selected from 7,400+ reviewers
- 📄 **Conducted 100+ paper reviews** across top robotics and CV venues

The review rules in these prompts reflect the standards expected at top robotics and computer vision venues, refined through real paper reviews and publications across ICRA, IROS, RSS, CVPR, ICCV, NeurIPS, AAAI, RA-L, T-RO, IJRR, T-PAMI, T-IV, etc.

______________________________________________________________________

## :page_facing_up: Files

### [`prompts/01_latex_workspace_review.md`](prompts/01_latex_workspace_review.md)

**LaTeX infrastructure audit** — detailed checklist for workspace-level errors before submission.

| Check | Description |
|-------|-------------|
| C1 | Preamble configuration (`hyperref`, `cleveref`, `caption` setup) |
| C2 | Package load order & conflicts |
| C3 | Macro safety, `\methodname` consistency, subscript macros, `\etalcite` |
| C4 | Cross-reference consistency (multi-ref, subcaption `Fig. 5(a)` format) |
| C5 | Label naming conventions, duplicate labels |
| C6 | Citation & bibliography integrity, duplicate BibTeX keys |
| C7 | Figure & table safety (missing files, dummy figures, label placement) |
| C8 | Hidden human errors (TODOs, inconsistent naming, `\vspace` hacks) |
| C9 | Academic writing patterns detectable in source (`\ie`, `\eg`, units) |

### [`prompts/02_paper_proofreading.md`](prompts/02_paper_proofreading.md)

**Paper content proofreading** — detailed checklist for strict conference-level review.

| Category | Description |
|----------|-------------|
| A | Language & grammar, tense consistency, Related Work tense |
| B | Language quality & awkward expression: typos, nominalization, filler phrases, citation-as-noun style |
| C | Scientific clarity: overclaiming, "significantly", unsupported claims |
| D | Structure & flow: intro claims, experiment purpose, equation narrative |
| E | Figure/table/caption review: self-containedness, reference order, quantitative consistency |
| F | LaTeX formatting: units, thousand separators, `\ie`/`\eg` macros |
| G | Abstract (WHY→PROBLEM→HOW→RESULTS) & conclusion quality |
| H | Notation consistency: symbol overload, boldface vectors, coordinate frames |
| I | Hyphenation: compound adjectives, `-ly` adverb rule |

### [`prompts/04_thesis_proofreading.md`](prompts/04_thesis_proofreading.md)

**PhD thesis proofreading (robotics)** — the paper checklist extended with checks for long, multi-chapter documents, from the perspective of an external examiner.

| Category | Description |
|----------|-------------|
| A | Thesis architecture: T-structure, chapters building on each other, research question traceability, consistent chapter structure |
| B | Chapter-level structure: chapter introductions and summaries, equation narrative, experiment purpose, real-robot validation |
| C | Paragraph flow and motivation reminders: paragraph logic, signposting, stale cross-references |
| D | Standalone and adjacent-field readability |
| E | Cross-chapter consistency and contradictions: claims, numbers, names, spelling variant, "we" vs "I" |
| F | Abbreviations across a long document: re-introduction after long gaps, per-chapter expansion, list of abbreviations |
| G | Heading hierarchy and casing: Title Case vs Sentence case, no lone subsections, stacked headings |
| H | Literature review coverage of every technical chapter, gaps, currency |
| I–P | Paper checks adapted to theses: language, paper leftovers ("in this paper"), claims, captions (short captions, attribution of reused figures), LaTeX, abstract/intro/conclusion, notation, hyphenation |
| Q | Front matter, back matter, and bibliography: statements of contribution, publication notices, appendices |

### [`prompts/05_highimpact_proofreading.md`](prompts/05_highimpact_proofreading.md)

**High-impact journal proofreading** — for Science Robotics, Science, Nature, Nature Machine Intelligence, and Nature Communications, from the perspective of the handling editor and three referees (domain expert, adjacent-field roboticist, broad reader). Self-contained; distilled from published neuromorphic and event-based robot vision papers, a Nature Masterclass, and real referee reports.

| Category | Description |
|----------|-------------|
| — | Story card: the advance in one sentence, breadth, "first" claim and evidence, headline numbers, top referee objections |
| A | Editorial triage: advance, significance, breadth of interest, the two-minute editor test |
| B | Article architecture: Intro → Results → Discussion → Methods, no Related Work section, required statements, length (verify against the guide) |
| C | Title, one-sentence summary, abstract ("Nature formula", headline numbers, honest comparisons) |
| D | Introduction funnel: broad hook, accessibility, concrete gap, "why this route", "Here we" |
| E | Results narrative: overview first, descriptive headings, aim → finding → meaning, failures, honest baselines |
| F | Claims and rigour: overclaiming ("first", "accurate", "scalable"), baselines and fairness, attribution, statistics |
| G | Domain module (toggleable): neuromorphic and event-based robot vision, energy and latency accounting, bio-inspiration |
| H | Discussion: recap, meaning, the major question, limitations, future, closing without hype |
| I | Figures, movies, captions: Figure 1 concept, bold caption titles, cross-references |
| J | Materials and Methods, supplement, data/code availability, statements |
| K–L | Language for a broad readership; numbers, units, notation, LaTeX, hyphenation |
| M | Submission package: cover letter, response to reviewers |

### [`prompts/06_perspective_proofreading.md`](prompts/06_perspective_proofreading.md)

**Perspective article proofreading (ecology and evolution)** — for Nature Ecology & Evolution Perspectives and similar opinion-led formats, from the perspective of the handling editor and three referees (subfield expert, ecologist from another subfield, applied reader). Self-contained; distilled from published Nature Ecology & Evolution Perspectives, the journal's format guidelines, and a Nature Masterclass.

| Category | Description |
|----------|-------------|
| — | Argument card: thesis in one sentence, Perspective type, novelty, why now, who cares, evidence breadth, counter-argument, forward look |
| A | Editorial triage: clear thesis, Perspective versus review, novelty, timeliness, breadth, the two-minute editor test |
| B | Format: 3,000–4,000 words, 4–6 display items (boxes count), no footnotes, ≤ 100 references, architecture, statements |
| C | Title and standfirst (stake → tension → "Here we" → moves → implication) |
| D | Introduction: concrete opening, concept defined against the established one, gap, "Here we" with roadmap |
| E | Argument structure: one argument built step by step, frameworks, theory, running example, ending |
| F | Balance, evidence, and hedging: counter-arguments, breadth of examples, calibrated language, equity |
| G | Forward look: roadmap, open questions, testable predictions, recommendations with named actors |
| H | Display items: concept figure, synthesis table, case-study and technical boxes, credits |
| I | References and intellectual heritage: crediting related concepts, citation fit, self-citation |
| J | Domain module (toggleable): aquatic and marine ecology and conservation policy |
| K–L | Language for a broad ecology readership; nomenclature, numbers, LaTeX, hyphenation |
| M | Pitch (presubmission enquiry) and submission package |

______________________________________________________________________

## :hammer: How to Use

There are two supported ways to use this repository.

### Setup — Clone this repo once

```bash
git clone https://github.com/LimHyungTae/awesome-claudecode-paper-proofreading.git ~/awesome-claudecode-paper-proofreading
```

### Option 1 — Claude Code direct prompt use

These prompts are used from **inside your paper workspace**, not from inside this repository.
The `@` file reference in Claude Code resolves paths relative to the directory where `claude` is launched.

### Step 1 — Navigate to your paper workspace and launch Claude Code

```bash
cd /path/to/your/paper
claude
```

### Step 2 — Run the workspace audit first

In the Claude Code session, reference the prompt by its **absolute path**, then attach your paper files:

```text
@~/awesome-claudecode-paper-proofreading/prompts/01_latex_workspace_review.md

@main.tex @shortcuts.tex
```

### Step 3 — Run the content proofreader

Provide the root `.tex` file and the compiled PDF. The prompt automatically instructs Claude to follow all `\input{...}` calls and read every included section file:

```text
@~/awesome-claudecode-paper-proofreading/prompts/02_paper_proofreading.md

@main.tex @paper.pdf
```

> **Why the PDF?**
> The compiled PDF lets Claude cross-check two things invisible in source alone:
> - **Figure placement** — figures displaced far from their in-text reference
> - **PDF-level annotations** — leftover review comments not yet resolved

### Step 4 — Decide which issues to fix

After Phase 1 output, respond with:

```text
discard 3, 7, 12    ← skip specific issues
fix all critical    ← fix only CRITICAL issues
proceed with all    ← fix everything
```

### Step 5 (theses) — Run the thesis proofreader

For a PhD thesis, use the thesis prompt instead of the paper prompt in Step 3. Provide the root `.tex` file and the compiled PDF; the PDF is needed for page distances, the List of Figures, and figure placement:

```text
@~/awesome-claudecode-paper-proofreading/prompts/04_thesis_proofreading.md

@thesis.tex @thesis.pdf
```

For long theses, `thesis-level only` and `show chapter X only` keep the review focused.

### Step 5b (high-impact journals) — Run the high-impact proofreader

For Science Robotics, Science, Nature, or Nature Machine Intelligence submissions, use the high-impact prompt instead of the paper prompt in Step 3. Provide the root `.tex` file, the compiled PDF, and, if available, the supplement, the cover letter, and the journal's current guide to authors (its limits override the prompt's defaults):

```text
@~/awesome-claudecode-paper-proofreading/prompts/05_highimpact_proofreading.md

@main.tex @paper.pdf @cover_letter.tex
```

`show category A only` gives a quick editorial triage (would the paper be sent to review?) before the full review. Disable Category G for papers outside neuromorphic and event-based robot vision.

### Step 5c (Perspectives) — Run the Perspective proofreader

For a Perspective (e.g., Nature Ecology & Evolution), use the Perspective prompt. Provide the root `.tex` file, the compiled PDF, and, if available, the pitch (presubmission enquiry) and any editor instructions (they override the prompt's defaults):

```text
@~/awesome-claudecode-paper-proofreading/prompts/06_perspective_proofreading.md

@main_perspective.tex @perspective.pdf @pe-presubmission_enquiry.md
```

`show category M only` checks the pitch on its own before it is sent. Disable Category J for Perspectives outside aquatic and marine ecology and conservation policy.

### Option 2 — Codex workspace setup with `prompts/`

Copy the `prompts/` directory into your paper or thesis workspace:

```bash
cp -R ~/awesome-claudecode-paper-proofreading/prompts /path/to/your/paper/
```

Launch Codex from the workspace root and point it at the prompt you want:

```
Follow prompts/01_latex_workspace_review.md for `main.tex`.
```

or

```
Follow prompts/04_thesis_proofreading.md for `thesis.tex` and `thesis.pdf`.
```

______________________________________________________________________

## :bulb: Design Principles

- **Detect first, fix later** — the agent never modifies files until the user explicitly confirms
- **Modular categories** — each check is a labeled block; reorder or disable by editing the table at the top of each prompt
- **Real-world patterns** — rules extracted from annotated paper reviews across ICRA, RA-L, AAAI, BMVC, and CVPR submissions
- **Non-native writer aware** — covers patterns common in papers by Korean/Japanese researchers
- **`figures/` vs `pics/`** — distinguishes final manuscript figures from raw image sources

______________________________________________________________________

## :computer: CI / Headless Use

This setup also works in CI or other non-GUI environments as long as the agent runs from the paper workspace and sees the relevant instructions.

Recommended pattern:

1. Check out your paper repository.
2. Copy in `prompts/`, or inline the prompt content into your workspace's `AGENTS.md`.
3. Ask the agent to run the workspace review or proofreading pass.

______________________________________________________________________

## :link: Related

- [paper-writing-checklist](https://github.com/LimHyungTae/paper-writing-checklist) — LaTeX workspace guidelines referenced by these prompts in Korean
