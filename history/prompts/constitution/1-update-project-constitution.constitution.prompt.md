---
id: 1
title: update-project-constitution
stage: constitution
date: 2026-01-02
surface: agent
model: claude-sonnet-4-5-20250929
feature: none
branch: master
user: iqra com
command: sp.constitution
labels: [constitution, setup, governance]
links:
  spec: null
  ticket: null
  adr: null
  pr: null
files:
 - .specify/memory/constitution.md
tests:
---

## Prompt

```
/sp.constitution

Project:
- Spec-driven book with embedded RAG chatbot

Core principles:
- Spec-first workflow using Spec-Kit Plus
- Technical accuracy from official sources
- Clear, developer-focused writing
- Reproducible setup and deployment

Key standards:
- Book written with Docusaurus and deployed on GitHub Pages
- RAG chatbot grounded only in book content or user-selected text
- Stack: OpenAI Agents/ChatKit, FastAPI, Neon Postgres, Qdrant Cloud
- Runnable, well-documented code

Constraints:
- GitHub-based source control
- No hallucinated responses
- End-to-end reproducibility

Success criteria:
- Live book on GitHub Pages
- Fully functional embedded RAG chatbot
- All specs implemented via Spec-Kit Plus
```

## Response snapshot

Constitution file updated with project-specific principles for the spec-driven book with RAG chatbot project. The following principles were defined:
1. Spec-First Workflow
2. Technical Accuracy and Source Verification
3. Test-First Development (NON-NEGOTIABLE)
4. Reproducible Setup and Deployment
5. Developer-Focused Experience
6. Quality and Security Standards

Technology stack requirements and development workflow were also specified, along with governance rules.

## Outcome

- ✅ Impact: Initial project constitution established with 6 core principles
- 🧪 Tests: N/A (documentation change)
- 📁 Files: Updated .specify/memory/constitution.md with project-specific content
- 🔁 Next prompts: Proceed with spec creation using /sp.specify
- 🧠 Reflection: Constitution provides clear governance framework for the project

## Evaluation notes (flywheel)

- Failure modes observed: N/A
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): Begin feature specification with /sp.specify