---
description: "Documentation maintainability, file size, topic boundaries, and reviewability rules"
applyTo: "**/*.md"
---

# Documentation maintainability rules

These rules apply to all Markdown documentation files in this repository — study notes, service reference pages, architecture guides, and instruction files. The goal is a documentation base that any contributor or student can read, navigate, and update without getting lost in monolithic files.

---

## 1. File size

Keep files small enough that a reviewer or reader can absorb the whole document in one sitting.

| Document type | Soft limit | Hard limit |
| --- | --- | --- |
| Module study notes (`docs/modules/**/*.md`) | 1,000 words (~150 lines) | 2,000 words (~300 lines) |
| Service reference pages (`docs/azure-services/**/*.md`) | 800 words (~120 lines) | 1,500 words (~250 lines) |
| Architecture / reference guides (`docs/references/**/*.md`) | 1,200 words (~180 lines) | 2,500 words (~350 lines) |
| Index and README files | 400 words (~60 lines) | 800 words (~120 lines) |

When a file approaches its soft limit, split it by topic or responsibility **before** adding more content. For example, if a service page grows too large, extract detailed comparison tables or sub-service workflows into dedicated reference files.

---

## 2. Section and paragraph size

Sections that are too long make scanning and revision difficult.

- **Soft limit:** 4 sentences per paragraph.
- **Hard limit:** 6 sentences per paragraph.
- **Section body soft limit:** 30 lines per subsection. If a section exceeds this, break it down using `###` subsections, bullet points, or comparison tables.
- Each paragraph should convey exactly one coherent thought.

---

## 3. One responsibility per page

Each page must have exactly one reason to exist.

- **One service per service page.** Do not combine Azure OpenAI and Azure AI Search on a single service page; give each service its own page and link them via `docs/references/` or relationship sections.
- **One module per module directory.** Group module-specific study notes inside the corresponding numbered folder under `docs/modules/`.
- **One theme per reference page.** A reference document should address a single cross-cutting theme (e.g., authentication patterns, evaluation metrics, or service comparison matrices).

---

## 4. Single concern per section

- A section should explain a concept, compare options, describe a workflow, or present an example — not all at once.
- Separate architectural concepts from configuration details.
- Avoid mixing exam trivia with foundational architectural knowledge; place certification tips in a dedicated subsection.

---

## 5. Visual density and scannability

Dense blocks of text fatigue readers and impede study recall.

- Every document longer than 300 words should include at least one visual element: a comparison table, a structured checklist, or a Mermaid diagram.
- If text lists three or more items with common attributes, convert it into a Markdown table.
- If a sequence involves three or more services interacting, provide a Mermaid diagram (`graph TD` or `sequenceDiagram`).

---

## 6. No dead content or speculative scaffolding

Only commit documentation that is accurate, reviewed, and directly useful for AI-103 exam preparation.

- **No empty placeholder pages.** Do not commit files containing only "TODO: Add content later" or empty heading skeletons.
- If a topic is planned but not yet written, document it in `docs/progress.md` or a module roadmap instead of creating an empty file.
- Do not commit commented-out Markdown blocks (`<!-- ... -->`). Version control preserves history.

---

## 7. Direct, plain language

Avoid filler, academic jargon, and unnecessary preamble.

- Lead with the answer or core takeaway.
- State facts directly without rhetorical questions or conversational filler.
- Avoid hedging words ("it seems", "probably", "arguably") when stating Azure service behaviors or certification facts.

---

## 8. Change scope

Each pull request or agent iteration should be reviewable in a single sitting.

- **Aim for diffs under 400 lines changed** (additions + deletions).
- If a task requires more than 400 lines (e.g., scaffolding an entire module with multiple pages), split it into independent steps (e.g., Step 1: index and overview; Step 2: core services; Step 3: reference comparisons).
- Each commit should do one thing and have a descriptive subject line.
- Do not mix structural reorganizations with content additions in the same commit.
