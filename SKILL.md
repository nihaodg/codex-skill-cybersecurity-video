---
name: html-video-competition-pipeline
description: Build visually polished HTML-first narrated videos and export final MP4 deliverables. Use when Codex should turn a topic, script, campaign theme, class project, speech, or competition brief into a finished video by: (1) planning scenes, (2) creating a stylish HTML motion prototype, (3) generating or attaching voiceover and subtitles, (4) exporting video through Remotion or an equivalent render path, and (5) checking sync, pacing, framing, and output quality before delivery.
---

# HTML Video Competition Pipeline

Use this skill as a workflow skill. Keep the process HTML-first, audio-aware, and QA-heavy.

## Core Workflow

### 1. Lock the Brief Before Building

Extract or decide these items first:

- Audience and use case
- Runtime target
- Aspect ratio
- Tone
- Whether subtitles are required
- Whether the user needs only an HTML preview or a final MP4

If the brief is vague, choose a sensible default and move forward. For competition-style work, favor:

- `1920x1080`
- `30fps`
- strong opening within the first 3 seconds
- clear ending hold for 2 to 4 seconds
- a total runtime short enough to stay focused

### 2. Default to an HTML-First Visual Prototype

If there is no existing video codebase, create a stylish HTML prototype first. Prefer a single HTML file for early iteration because it is fast to preview, easy to tweak, and good for visual direction.

When building the HTML prototype:

- choose a strong visual direction instead of generic dashboard styling
- define a clear type scale, color system, and motion language
- make the opening scene feel immediate and memorable
- vary scene layouts so the whole piece does not feel like repeated slides
- preserve mobile-safe and title-safe margins even when the target is desktop video
- keep files and naming simple enough to port into a video pipeline later

If there is already a Remotion or other video project, adapt the existing structure instead of forcing a standalone HTML file.

### 3. Define Scenes Before Rendering

Write a scene manifest before generating final media. Each scene should have:

- scene id
- visual goal
- on-screen text
- narration text
- expected emotional beat
- approximate lead-in and tail hold

Do not begin with one monolithic narration track if sync matters. Split narration by scene and let actual audio lengths drive scene timing later.

For a history, explainer, or competition video, structure the scene flow like this:

- opening hook
- context or setup
- 2 to 4 development scenes
- climax or present-day relevance
- closing slogan or takeaway

Read [references/scene-blueprint.md](references/scene-blueprint.md) when scene structure, subtitle density, or narration chunking needs guidance.

### 4. Generate Voiceover and Subtitles from the Same Source

Create narration from the scene manifest, not from independently rewritten copy. The subtitle source and the voiceover source should stay aligned.

Use these rules:

- generate one audio file per scene when possible
- measure real audio duration before locking final scene lengths
- add a small lead-in before narration starts
- add a short hold after the sentence ends so cuts do not feel abrupt
- keep subtitles to two lines max
- prefer short subtitle chunks over full-paragraph blocks

If narration feels out of sync, fix scene timing or split the narration again. Do not only drag an entire long track across the timeline.

Read [references/render-qa.md](references/render-qa.md) when diagnosing sync, pacing, or audio balance issues.

### 5. Assemble in a Repeatable Video Pipeline

Prefer Remotion when any of these are true:

- frame-accurate sync matters
- multiple render iterations are expected
- subtitles should be burned in
- the user wants a durable project instead of a one-off recording

When assembling:

- keep background bed audio on its own track
- sequence narration scene-by-scene
- derive composition duration from actual scene timing
- keep captions tied to the same timing source as narration
- render preview frames and at least one preview video before final export

If Remotion is not available or is blocked, keep the HTML prototype as the design source and use a fallback export path. The fallback still needs QA.

### 6. Run a QA Loop Before Delivery

Always inspect output before calling the job done. Check:

- opening impact
- readability
- subtitle timing
- narration-to-scene sync
- dead air
- audio masking
- repeated layouts
- abrupt cuts
- safe margins
- final file existence and duration

If there is a problem, fix the source timeline and rerender. Do not hand off a render that was never checked.

Read [references/workflow-checklist.md](references/workflow-checklist.md) for a compact end-to-end checklist.

## Deliverables

Aim to leave behind:

- HTML prototype or source project
- scene manifest
- narration script
- scene-level audio files when available
- subtitles if requested
- final MP4
- a short QA summary mentioning what was verified
