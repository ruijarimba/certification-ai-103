# GitHub Copilot instructions for certification-ai-103

This repository contains study notes and reference documentation for the Microsoft AI-103 (Azure AI Apps and Agents Developer Associate) certification. Read this file and the linked instruction files before generating or modifying any documentation or repository content.

## Active instruction files

- `.github/instructions/agent-behaviour.instructions.md` — **read first** — agent behaviour, safety, and collaboration rules that apply to every task.
- `.github/instructions/certification-content.instructions.md` — AI-103 content authoring rules, module structure, and service page standards.
- `.github/instructions/documentation.instructions.md` — writing guidance for Markdown files; plain English, structure, and scannability.
- `.github/instructions/markdown.instructions.md` — Markdown syntax, formatting, lists, tables, and link rules.
- `.github/instructions/documentation-maintainability.instructions.md` — file size limits, topic boundaries, paragraph discipline, and change scope rules.

## Durable project context (read first)

- `README.md` — repository purpose and high-level folder structure.
- `docs/progress.md` — current session state, recently completed work, and next steps.
- `docs/glossary.md` — single source of truth for Azure AI domain terms and acronyms.
- `docs/modules/README.md` — index of certification modules.
- `docs/azure-services/README.md` — index of Azure service reference pages.
- `docs/references/README.md` — cross-module references, architecture comparisons, and relationship notes.

## Product scope boundaries

- This repository is documentation-first. Do not add code samples, sample applications, infrastructure code, Terraform, automation scripts, or CI/CD pipelines unless explicitly requested.
- Use the companion repository in this workspace only as a source for Copilot customization patterns. Do not copy its product content, .NET guidance, Model Context Protocol details, Azure Pipelines documentation, build rules, test rules, packaging rules, or solution-file conventions into this repo.

## Content standards

- **Original content only:** Summarize certification content in original words. Never copy Microsoft Learn passages verbatim into this repository.
- Brief descriptions of Azure services are allowed and encouraged when they are original, accurate, and linked to official Microsoft documentation.
- When you need Microsoft documentation or reference material, use the Microsoft Learn MCP server first, then verify important details against the linked Microsoft Learn page.
- Prefer concise notes, comparison tables, Mermaid diagrams, and decision matrices that aid study and recall.
- Keep module notes separate from Azure service reference pages: modular concepts go in `docs/modules/`, reusable service references go in `docs/azure-services/`.

## Safety and agent behaviour reminders

The canonical rules are in `.github/instructions/agent-behaviour.instructions.md`. Key reminders:

- **Never** perform irreversible actions (delete branches, force-push, expose secrets) without explicit human approval.
- **Agents propose; humans decide.** Present a plan before multi-file or structural edits. Silence is not consent.
- **Epistemic honesty:** say *"I don't know"* or *"I need more context"* when uncertain rather than guessing or hallucinating service features or exam syllabus details.
- **Minimal footprint:** do only what the task strictly requires. No extra files or speculative scaffolding.
- **Keep documentation synchronized:** when modules, services, or repository conventions change, update the corresponding index READMEs, `docs/progress.md`, and `docs/glossary.md` in the same change.

## Communication efficiency

- Keep agent communication token-efficient: avoid narrating every tool call or intermediate thought.
- Do not repeat plans, status, or file contents unless changed or requested.
- Batch independent actions into one turn when possible, and report progress using numbered plan steps or concrete file counts.
