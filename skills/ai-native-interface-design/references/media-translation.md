# From component to artifact, creative, image and video

Share content and visual roles, not identical pixel layouts. A code artifact is a working stateful object; a campaign creative is an editorial composition; an image is a frozen state; a demo video is an ordered sequence. Preserve data meaning across all four.

## Interactive artifacts

Build a small complete interaction, not a wall of disconnected examples. Include a visible simulation label if data is fictional, a reset/replay control if sequenced, and evidence disclosure. Respect the intended runtime: a standalone file should not silently depend on remote fonts, packages or build tooling. When embedding in an existing app, retain its navigation and semantics.

## Campaign creatives

Choose one message and a hero component that proves it visually. Put promotional language outside the product frame. A 1200×628 landscape or 1080×1350 portrait is a drafting option when no channel is specified, not a universal export requirement. Crop secondary chrome, enlarge the finding and preserve context. Keep logos as original supplied artwork, not recreated text or generated symbols.

A useful layout: short outcome-led headline, focal answer card, small evidence rail, optional CTA. Avoid statistics about productivity/accuracy unless sourced. Data inside the component is not evidence of customer impact.

## Images

For exact UI text, numbers, SQL and logos, render HTML/SVG or use an approved product capture when tools allow. Use image generation for conceptual treatments and imagery; specify exact copy but inspect the returned image because prompts do not guarantee fidelity. Use the available image-editing workflow for edits. Do not call generated concept UI a screenshot of the real application.

Suggested prompt structure:

> Produce a [dimensions/aspect] [concept UI/product marketing] composition for [audience]. Main message: [one sentence]. Focal object: [component and completed state]. Layout: [placement and hierarchy]. Surface/ink/accent roles: [brand tokens]. Exact visible copy: [short strings]. Data: [consistent values, period, units]. Evidence treatment: [source label]. Keep [logo area] reserved for supplied artwork. Render controls as [static concept or actual captured UI].

For legible data-heavy output, prefer a deterministic render. Request no extra labels or invented metrics. Inspect at intended display size, not just zoomed in. Deliver the actual image when requested, plus editable source if created.

## Demo videos

First distinguish a recording of the real product from an animated concept. Use an actual product capture for literal capabilities and current UI. Label staged data and concept frames. An animated example must not imply measured backend speed; identify time compression where relevant.

Create a shot list with start/end, component state, on-screen action, pointer/focus, narration, and hold time. Suggested 20-second concept:

| Time | Scene | Purpose |
|---|---|---|
| 0–3s | Business question already readable | Establish task without slow typing |
| 3–6s | Compact observable query activity | Show transition; simulated timing is disclosed |
| 6–12s | Answer + chart/table | Hold the result long enough to read |
| 12–16s | Expand SQL or evidence | Demonstrate inspectability |
| 16–20s | Select a meaningful follow-up or hold closing result | Show next useful step |

Adapt duration to copy and audience; do not accelerate unreadable text to fit. Freeze dates and use one deterministic timeline; avoid autoplay carousels changing independently. Move the pointer to actual targets; no decorative aimless cursor. Keep captions within platform safe areas and away from metrics. For portrait, recompose to one pane rather than cropping the desktop center blindly.

If the user asks for a rendered video, use available recording/rendering tools and verify output dimensions, duration, first/last frames and a key transition. A storyboard, HTML animation or AgentScreen recording counter is not an MP4. If rendering is unavailable, state that and deliver the storyboard and editable scene source without claiming a video was made.

## Cross-format review

- Same business question, metric definition, dates, scope, units and arithmetic.
- Static outputs show a meaningful resolved state, not a cut-off loading sentence.
- Charts retain baselines, labels and truthful shape; cropping never changes the claim.
- Mock verification and sample data remain visibly illustrative in the exported frame.
- Text survives actual-size viewing and compression; use fewer rows rather than illegible font sizes.
