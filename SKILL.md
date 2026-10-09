---
name: video-production-agent
description: "A compact router for creating, editing, regenerating, or reviewing videos and media assets. Use with an already-configured AI environment; loads only the relevant specialist instructions from the linked editing and generative-media repositories, asks minimal essential questions, executes, and verifies actual outputs."
---

# Video Production Agent

Use the smallest relevant context to complete the user's video task. The environment is assumed to be configured; do not reinstall or run a broad setup audit without a task-specific reason.

## Route

- Editing, story, motion, captions, audio, render, editorial QA → [video-editing-skills](https://github.com/adittaya/video-editing-skills). Read `HARNESS.md`, one best-fit `skills/<name>/SKILL.md`, then only needed sections of its detailed guide.
- Generation or remote inference → [local-generative-colab-skill](https://github.com/adittaya/local-generative-colab-skill). Read `references/workflow-contract.md` and only the relevant parts of `SKILL.md` and one specialist reference.
- Mixed job → combine both routes at the handoff; generation owns model/backend execution and artifact retrieval, editing owns creative decisions, timeline, finishing, and editorial review.

## Behaviour

1. Infer reasonable defaults from the request and supplied assets. Ask only questions whose answers materially change the result or unblock work; group any necessary questions into one short message.
2. Never load either repository wholesale. Read guide headings first; retrieve only relevant sections. Do not run a full feature checklist or force effects to satisfy a quota.
3. Keep work proportional: skip unnecessary documents, asset packs, contact sheets, and approval gates for simple jobs. For complex work, plan briefly and validate a representative slice before scaling when useful.
4. Verify only task-critical capabilities; never assume credentials, quota, models, remote jobs, or GPU access. Preserve source files, rights, privacy, and provenance.
5. Verify the actual outputs before claiming completion. Report output paths, evidence of checks, and limitations honestly.

The human-facing session prompt and first-response instruction are in the repository README. This skill does not install tools or guarantee quality.
