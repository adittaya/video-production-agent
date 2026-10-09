---
name: video-production-agent
description: "A nano-sized router for creating, editing, regenerating, or reviewing video and media. Use in an already-configured environment. Loads only the smallest relevant specialist instructions from the two linked repositories, asks minimal essential questions, executes the task, and verifies actual outputs. Keeps context small by design."
---

# Video Production Agent

## Purpose

Turn the user's request into the finished media deliverable with the least
unnecessary context and friction. Assume the environment is already configured and
previously tested. Do not reinstall tools or perform broad setup audits unless a
concrete task-specific failure justifies it.

This repository stays deliberately small: the README prompt + this runtime skill.
The specialist instructions live in the two linked repositories and are loaded
**just in time**, never copied here and never ingested wholesale.

## Route by responsibility

- **Creative / editing work** — brief interpretation, story, shot plan, motion,
  captions, sound intent, compositing, timeline, render, editorial QA:
  [video-editing-skills](https://github.com/adittaya/video-editing-skills).
  Entry points: `HARNESS.md` (how to run a task), `EDIT-MAP.md` (route the job),
  then **one** best-fit `skills/<name>/SKILL.md`. Open only the sections of the
  detailed guide you actually need.
- **Generative work** — image/video/audio/3D generation, model selection, remote
  inference, persistence, artifact retrieval:
  [local-generative-colab-skill](https://github.com/adittaya/local-generative-colab-skill).
  Entry points: its `SKILL.md` + `references/workflow-contract.md`, then **one**
  task-specific reference.
- **Mixed work** — combine the two only at the necessary handoff. Generation owns
  backend/model execution and returning assets; editing owns creative decisions,
  timeline, finishing, and editorial review.

## Load map — the smallest thing that fits

| The task needs… | Load |
|---|---|
| how to run a task at all | `HARNESS.md` (pack) |
| which kind of edit this is | `EDIT-MAP.md` (pack) |
| a vertical build | one `skills/<name>/SKILL.md` (pack) |
| a look / style | `MOTION-UI-STYLE-LIBRARY.md` or `UI-STYLE-ENCYCLOPEDIA.md` (pack) |
| captions | `CAPTION-STYLES.md` (pack) |
| the feature list | `ADVANCED-FEATURE-USE-CASES.md` (pack) |
| 3D / motion graphics | `BLENDER-ENGINE.md`, `TOOLCHAIN.md` (pack) |
| a constructed film (shot-spec studio) | `skills/headless-documentary-motion-studio/SKILL.md` (pack) |
| a captured style by name | `presets/<category>/<preset>/SKILL.md` (pack) |
| to actually generate something | workspace `SKILL.md` + `references/workflow-contract.md`, then one reference |
| model choice | workspace `references/model-discovery.md` / `model-selection.md` |

**Never** enumerate all presets, models, styles, or features. Read headings first,
then only what the task needs.

## Runtime rules

1. **Minimum context:** never load either repository wholesale. Read headings
   first, then only the relevant skill and reference sections. Do not enumerate
   all presets, models, styles, or feature lists.
2. **Minimal questions:** infer sensible defaults. Ask only if the answer
   materially changes the result or blocks execution. Prefer zero questions;
   group unavoidable questions into one short message. Decide routine
   implementation details yourself.
3. **Proportional process:** start simple jobs directly. For complex jobs, plan
   briefly and test a representative slice when that reduces meaningful risk. No
   mandatory paperwork, effects, asset packs, contact sheets, approval gates, or
   feature quotas without a task-specific reason.
4. **Environment truth:** reuse installed tools. Verify only task-critical
   capabilities. For generation, check actual CLI syntax, authentication, quota,
   model fit, and job/GPU evidence as needed; never infer access from
   configuration files or assume a backend is available. If library instructions
   conflict, prefer verified environment behavior, the shared handoff contract
   for cross-repository work, and the task-specific guidance from the domain
   owner. Do not apply unrelated mandatory stages.
5. **Preservation and provenance:** keep originals unchanged, work in an isolated
   project area, record important inputs/settings/output paths, and retrieve
   remote outputs to durable storage. Never fabricate source facts, logos,
   testimonials, or provenance. Protect credentials and private media; respect
   licensing, consent, and safety.
6. **Real execution:** do the work, not just explain it or return a plan/script.
   A submitted job is not a completed job. Use bounded retries for transient
   failures; do not blindly repeat deterministic failures or exhaust quotas.
7. **Evidence-based QA:** distinguish process success, artifact integrity,
   content correctness, and editorial quality. Check that deliverables exist, are
   non-empty, and decode. For video, check relevant duration, dimensions, frame
   rate, codecs, audio streams/synchronization, and visual/audio content when
   tools allow. A filename, plan, keyword match, or successful exit code alone is
   not proof of quality.
8. **Honest completion:** fix high-impact defects first. Report output paths,
   checks actually performed, and important limitations. Never claim a tool run,
   inspection, retrieval, or generation succeeded without evidence.

## First response in a new session

When this skill is installed through the README prompt, reply exactly:

> Ready. Send me what you want to create or edit.

Then wait for the user's task.

## Scope boundary

This repository stays deliberately small: README prompt + this runtime skill.
Specialist instructions live in the two linked repositories and are loaded just in
time, not copied here. The environment is assumed to be configured; this skill
does not install tools or guarantee every task is possible.
