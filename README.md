# HTML Video Competition Pipeline

A reusable Codex skill for building polished, HTML-first narrated videos and exporting final MP4 deliverables.

This skill is designed for workflows like:

- competition videos
- history or science explainers
- school presentation videos
- campaign or event promo videos
- topic-to-video rapid prototyping

It helps an agent follow a stable pipeline:

1. understand the brief
2. build a strong HTML visual prototype
3. plan scenes
4. generate or attach voiceover
5. assemble and export the video
6. review sync, pacing, framing, subtitles, and final quality

## Can Anyone Use This Skill?

Yes, with a small caveat:

- Anyone using a Codex-compatible skill system can reuse this skill.
- It is portable because the main workflow lives in `SKILL.md` and the supporting references live in `references/`.
- To use the full video pipeline, the environment should support HTML editing plus a video render path such as Remotion.
- For AI voiceover generation, network access or a local TTS tool may be required.

So the short answer is: yes, other people can use it, but they still need a compatible runtime and the tools required by their chosen render / TTS workflow.

## What This Skill Does

This skill tells Codex to:

- default to an HTML-first visual prototype
- avoid generic, boring layouts
- split the video into scenes before rendering
- keep narration, subtitles, and scene timing aligned
- use per-scene audio timing when sync matters
- prefer a QA loop before delivery
- export a final MP4 only after checking the result

## Repository Structure

```text
html-video-competition-pipeline/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── render-qa.md
    ├── scene-blueprint.md
    └── workflow-checklist.md
```

## Main Files

- `SKILL.md`
  The actual skill definition and workflow instructions.

- `agents/openai.yaml`
  UI-facing metadata for Codex-compatible environments.

- `references/workflow-checklist.md`
  A compact end-to-end checklist for production and delivery.

- `references/scene-blueprint.md`
  A scene planning template for keeping visuals, narration, and subtitles aligned.

- `references/render-qa.md`
  Troubleshooting guidance for sync, pacing, audio balance, and visual repetition.

## Installation

Place this folder into a Codex skill directory, for example:

```text
$CODEX_HOME/skills/html-video-competition-pipeline
```

or, if `CODEX_HOME` is not set:

```text
~/.codex/skills/html-video-competition-pipeline
```

If your setup supports local skill loading from a workspace, you can also keep the folder inside a project and point Codex at it explicitly.

## Example Usage

Typical prompts:

```text
Use $html-video-competition-pipeline to make a cyber security history competition video.
```

```text
Use $html-video-competition-pipeline to turn this speech into a narrated MP4 with subtitles.
```

```text
Use $html-video-competition-pipeline to build a stylish HTML prototype first, then add voiceover and export video.
```

## Recommended Workflow

This skill works best when the agent follows this order:

1. lock the topic, audience, runtime, and aspect ratio
2. create a strong HTML prototype
3. write a scene manifest
4. generate narration from the scene structure
5. measure real audio duration
6. align scene timing to the audio
7. export preview frames or preview video
8. fix sync and pacing problems
9. export the final MP4

## Requirements and Assumptions

The exact toolchain is flexible, but full use usually assumes:

- a Codex environment with skill support
- the ability to edit HTML/CSS/JS
- a render path such as Remotion for frame-accurate video output
- optional TTS support for AI narration
- optional media probing / QA tools for checking final files

## Notes

- This skill is workflow-oriented, not template-locked.
- It is meant to guide an agent through a reliable production process rather than force one exact visual style.
- It is especially useful when video quality depends on sync, pacing, and iterative QA rather than just generating a single HTML page.

## License

Add your preferred license before publishing if you want others to reuse, modify, or redistribute it under clear terms.
