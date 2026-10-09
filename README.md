# Video Production Agent

An **all-in-one, self-contained** video production agent. Hand it a source — a
brief, a script, a voiceover, or a reference video / contact sheet — and it plans,
generates the assets, and builds the finished video **headlessly**.

It carries **both halves** in one file: an **editing engine** (Blender 3D,
Remotion 2D motion graphics, FFmpeg) **and** a **generative workspace** (a remote
Colab/Kaggle GPU for image reconstruction, matting, 3D, audio, voice and video
generation). **Everything the agent needs is in `SKILL.md`.** One repo, one skill —
it depends on no *other* repository, no other links, nothing to fetch.

**Repo:** https://github.com/adittaya/video-production-agent
```
git clone https://github.com/adittaya/video-production-agent.git
```

```
video-production-agent/
  SKILL.md     the whole skill — all in one, self-contained
  README.md    this file — the prompt
```

## Use it

Point your AI at this repo, then paste the prompt below and send your **source**.

```text
You are the "video-production-agent".

GET YOUR SKILL. It lives in this repository:
    https://github.com/adittaya/video-production-agent
Clone it (git clone https://github.com/adittaya/video-production-agent.git), or
read it directly:
    https://raw.githubusercontent.com/adittaya/video-production-agent/main/SKILL.md
Then READ SKILL.md IN FULL. SKILL.md is your entire skill — it is ALL IN ONE and
self-contained: it holds everything you need (the pipeline, the engines, the look,
the features, the two asset prompts, the laws, the gates). Depend on NOTHING else
— no other repositories, no other links, no fetching anything outside this one
file. This repository is the only thing you need.

FIRST REPLY — reply exactly this, then wait:
    Ready. Send me what you want to create or edit.

Then run the pipeline in SKILL.md: SOURCE -> PLAN -> ASSETS -> A-ROLL -> BUILD ->
QA, working headless and programming your tools (Blender for 3D, Remotion for 2D
motion graphics, FFmpeg for media). Two asset prompts, always separate (visual +
sound). Prep the A-roll background first when a person speaks. Show contact-sheet
variants V1/V2/V3 before rendering, then QA and deliver.

Be decisive and quality-first. Do the work — do not stop at a plan. Never invent
facts, quotes, logos or stats, and never clone a voice or likeness without consent.

Start now with your FIRST REPLY, then wait for my source.
```

## What it does

```
SOURCE (brief · script · voiceover · reference · contact sheet)
  -> PLAN        CONCEPT.md  (thinking + style + feature passes)
  -> ASSETS      ASSETS-VISUAL.md + ASSETS-SOUND.md   (two prompts, separate)
  -> A-ROLL      you supply it (voiceover / avatar / podcast)
  -> BUILD       Blender (3D) + Remotion (2D) + FFmpeg  — headless
  -> QA          contact sheets V1/V2/V3  +  EDIT-QA.md
  -> FINISHED VIDEO
```

## The laws it keeps

Extract don't guess · program don't click · A-roll prep first when a person speaks
· the look is chosen, not mandated · text maps the visual · construct
deterministically and inspect · never invent · never clone a voice without consent.
