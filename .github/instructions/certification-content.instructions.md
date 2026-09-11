---
description: "AI-103 certification content authoring rules, module structure, and service page standards"
applyTo: "docs/**/*.md"
---

# Certification content authoring rules

These rules govern how AI-103 certification notes, module summaries, service references, and architecture guides are authored in this repository.

The goal is to produce high-yield, structured, original study materials that help a student prepare thoroughly for the Microsoft Certified: Azure AI Apps and Agents Developer Associate (AI-103) exam.

---

## 1. Content focus and scope

- Focus on **certification content**: core concepts, Azure AI architectural patterns, service capabilities, decision boundaries, integration workflows, and security models.
- Do not create a separate or redundant exam-objectives syllabus tracker; instead, ensure that the module notes directly reflect the knowledge and capabilities tested in each certification module.
- Keep the repository documentation-first. Do not add full code applications, infrastructure code, or deployment scripts in `docs/` unless a brief snippet clarifies a concept.

---

## 2. Source handling and Microsoft Learn policy

- **Strict anti-plagiarism rule:** Never copy passages, paragraphs, or exercise text verbatim from Microsoft Learn, exam dumps, or third-party training courses.
- Summarize all concepts, processes, and service descriptions in original words.
- Brief, original summaries of Azure services are required. Always link directly to the official Microsoft Learn documentation page for definitive product behavior, limits, and tutorials.
- Verify product names, current SKUs, supported model versions, and API behaviors against authoritative Microsoft documentation before committing.

---

## 3. Module documentation structure (`docs/modules/`)

Organize certification modules into numbered directories with descriptive slugs:

```text
docs/modules/
├── 01-plan-and-manage-an-azure-ai-solution/
│   ├── README.md
│   └── ...
├── 02-implement-generative-ai-solutions/
└── ...
```

Each module page or module README should follow this standard structure:

1. **Overview & learning focus:** Brief 2-3 sentence summary of what this module covers for the AI-103 exam.
2. **Key concepts & architectures:** Theoretical foundations and service building blocks.
3. **Core workflows:** Step-by-step conceptual walkthroughs of key tasks (e.g., creating a fine-tuning job, configuring a vector search index, deploying an agent).
4. **Service relationships:** How the services in this module interact with one another.
5. **Exam decision factors:** "When to choose service X vs service Y" matrices or trade-off tables.
6. **Security, governance & monitoring:** RBAC roles, managed identities, Content Safety filters, network isolation, Application Insights telemetry.
7. **Official resources:** Direct links to the relevant Microsoft Learn documentation paths.

---

## 4. Azure service reference pages (`docs/azure-services/`)

Every relevant Azure service in the AI-103 syllabus has a dedicated reference page in `docs/azure-services/` (e.g., `azure-ai-foundry.md`, `azure-openai.md`, `azure-ai-search.md`).

Each service page must contain:

- **Service purpose:** Plain-English summary of what the service does and why it exists.
- **Role in AI-103:** Specific exam scenarios and capabilities where this service appears.
- **Key features & capabilities:** Main capabilities, model types, API operations, or tooling options.
- **Relationships to other services:** Table or diagram showing integration points (e.g., Azure AI Search as a knowledge base for Azure OpenAI RAG).
- **Security & identity:** Default authentication methods (Entra ID, API keys), Key Vault integration, and network security.
- **Trade-offs & limitations:** Quotas, regional availability considerations, or pricing tier distinctions relevant to the exam.
- **Official references:** Canonical links to Microsoft Learn product documentation.

---

## 5. Visual diagrams and comparison tables

- **Mermaid diagrams:** Every multi-service workflow, agent pipeline, or RAG pattern must include a top-down Mermaid diagram (`graph TD`).
- **Comparison tables:** Use comparison tables whenever two similar services, tools, or SKUs could be confused on the exam (e.g., Azure AI Foundry vs Azure OpenAI Studio; Prompt Flow vs Semantic Kernel / LangChain; Basic vs Standard Azure AI Search SKUs).
- Keep tables concise and scannable, focusing on differences that affect architectural decisions.

---

## 6. Terminology and glossary alignment

- Align all terminology with `docs/glossary.md`.
- Introduce and link domain terms (e.g., RAG, Grounding, System Prompts, Chunking, Vector Embeddings, Temperature, Top-P, Semantic Ranking) on their first appearance.
- Spell out acronyms on first use per `markdown.instructions.md`.

---

## 7. Review and quality checklist

Before committing any certification study page:

- [ ] Is the content completely original and not copied verbatim from Microsoft Learn?
- [ ] Are all relative links resolving to valid existing documentation files?
- [ ] Are external links pointing to authoritative official Microsoft Learn URLs?
- [ ] Is every service mentioned linked to its dedicated page in `docs/azure-services/`?
- [ ] Does the page comply with `markdown.instructions.md` and `documentation.instructions.md`?
- [ ] Is the page listed in the appropriate folder index (`README.md`)?
