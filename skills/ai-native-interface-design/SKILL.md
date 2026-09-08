---
name: ai-native-interface-design
description: Design polished AI interface components and translate them into interactive artifacts, campaign creatives, images, and demo-video storyboards. Use for prompting, progress, evidence, results, and human decisions; includes an optional Databricks Genie profile.
---

# AI-native interface design

Build a coherent interaction story: question → observable work → supported result → useful next action. Draw from Beautiful UI's compact, layered components without assuming its demo behaviors are production features. The user’s product, brand, medium and requested fidelity govern the result.

## Choose the working context

Extract the intended audience, outcome, medium/aspect ratio, real versus illustrative data, and fidelity (actual product capture, concept UI, or abstract creative). Infer ordinary defaults and state consequential assumptions. Ask only when an answer materially changes the deliverable. For an unspecified artifact, start with a responsive interactive HTML concept; for an image or video, choose dimensions appropriate to the requested channel and document them.

Read project design.md/DESIGN.md or supplied brand assets if available. Keep marketing framing separate from literal product UI. For Databricks Genie, read [the Genie profile](references/databricks-genie.md); otherwise do not import its colors, terms, or scenario.

## Compose the smallest useful system

Read [visual grammar](references/visual-grammar.md) and choose from [component patterns](references/component-patterns.md). Select components by the user decision they support, not by how many fit on the canvas. Usually a prompt, concise progress summary, answer/evidence block and next action are sufficient. Add navigation, tables, inspectors or a second pane only when the task warrants them.

Define the component's content, state, evidence and actions before styling. Share one content fixture across all requested media. Use [the brief template](assets/component-brief.md) when the work benefits from a written contract; use [the illustrative Genie fixture](assets/genie-revenue-scenario.json) only for an explicitly fictional demo or concept.

Route by deliverable:
- **Interactive artifact / implemented component:** read [implementation guidance](references/implementation.md). Reuse the existing stack; native HTML/CSS is sufficient for a compact demo. The optional [token starter](assets/tokens.css) is dependency-free and scoped; it is a proposed baseline, not official product CSS.
- **Creative / image / video:** read [media translation](references/media-translation.md). Preserve the same question, metric, evidence and state across formats. Use actual available image/video tools when rendering is requested; a prompt or storyboard alone is not a rendered asset. State any tool limitation and deliver the concrete work possible.
- **Direct reuse of Beautiful UI code:** first read [source audit](references/source-audit.md), including license and implementation seams. Do not install the full upstream app to borrow a visual pattern.

## Essential behavior

Use observable activity summaries (for example, “Running query”) instead of invented private reasoning. Show counts, durations, provenance and “verified” labels only when supported by real metadata, or visibly label the entire fixture as illustrative. A UI animation is not proof that work occurred.

In live components, render actual state transitions. Separate empty results, partial results, missing access, failure, cancellation and success where they can occur. Keep partial content identifiable. Retrying must not turn an old failure into success by elapsed time. Preserve user-entered context and manual expansion choices.

A clarifying question and authorization to change something are different interactions. For a consequential action, show the exact proposed change and an explicit commit control; selecting an option or waiting must not execute it. Avoid adding approval screens to ordinary read-only exploration.

## Review and deliver

Inspect at final display size, with long text and narrow layouts. For interactive work, verify the primary path, an applicable failure/recovery path, keyboard operation, focus visibility and reduced motion. For static work, verify legibility, chart meaning, provenance and clear distinction between concept UI and an authentic capture. For video, check key frames and that the result remains readable long enough.

Keep implementation-notes.html in the output project for design decisions, deviations, tradeoffs and open questions; append a scoped section when the file already exists. Deliver the requested artifact plus the few material assumptions or limitations. Do not claim a render, integration or test that was not performed.
