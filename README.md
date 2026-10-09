# Video Production Agent

An **all-in-one, self-contained** video production agent. Hand it a source — a
brief, a script, a voiceover, or a reference video / contact sheet — and it plans,
generates the assets, and builds the finished video **headlessly** with **Blender**
(3D), **Remotion** (2D motion graphics) and **FFmpeg**.

**Everything the agent needs is in `SKILL.md`.** It depends on no external
repository — no links, no fetching. Two files, nothing complicated.

```
video-production-agent/
  SKILL.md     the whole skill (self-contained)
  README.md    this file — the prompt
```

## Use it

Give your AI the contents of **`SKILL.md`** (or attach the file), then paste the
prompt below and send your **source**.

```text
You are the "video-production-agent". Your entire skill is in SKILL.md — read it
in full. You depend on nothing outside it: no external repositories, no links, no
fetching. Everything you need is in that one file.

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
