# Databricks Design

A design framework for creating Databricks components, presentations, documents, and marketing assets with AI-assisted authoring.

## The two parts

| Resource | Responsibility |
| --- | --- |
| [design.md](design.md) | Databricks visual identity, typography, colors, logo rules, component guidance, and documented source gaps |
| [Layered Grid Design skill](skills/layered-grid-design/SKILL.md) | Composition through spacing rhythm, safe areas, content groups, structure, and typography, followed by rendered review |

Use both when building assets. The skill applies a layout method within the design system; established brand rules and supplied templates take precedence over its optional defaults.

## Build an asset

Give the authoring assistant the brief, audience, content, output dimensions, relevant brand assets or template, and both resources above. In Codex, use `$layered-grid-design` when the skill is installed; otherwise point the assistant directly to its SKILL.md.

Example prompt:

> Read design.md and skills/layered-grid-design/SKILL.md. Create a Databricks Genie marketing carousel for business leaders using the supplied messaging and product references. Establish the spacing rhythm, safe areas, content groups, and structural layout before typography and final styling. Preserve Databricks fonts, palette, and logo rules. Keep shared anchors across slides while varying composition to suit the message. Render at the intended viewing size, correct clipping and hierarchy problems, and record material interpretations in implementation-notes.html.

Specify the actual carousel dimensions and slide count in the brief. Replace the output format and subject for presentations, documents, interface components, or other assets.

## Databricks application rules

- Use DM Sans for the brand's primary typography and DM Mono for code where applicable, as described in design.md. Do not replace them with the source example's Inter/Baskerville pairing.
- Follow supplied templates and established component tokens first. Where spacing or radius rules are missing, label chosen values as proposed; do not present the 8px unit or 24px radius/inset as official Databricks tokens.
- Start with up to three sizes and three weights per coherent component. Preserve readability, semantic structure, and established styles when they require a documented exception.
- Adapt the grid to native units and viewing conditions for slides, print, documents, and social images. Do not copy screen-component pixel values into every medium.
- Inspect the rendered result. A valid file or a consistent token list does not establish effective communication.

## Skill resources

- [Layout contract](skills/layered-grid-design/references/layout-contract.md): record geometry, roles, provenance, and exceptions.
- [Medium adaptation](skills/layered-grid-design/references/medium-adaptation.md): apply the method to each output format.
- [Source examples](skills/layered-grid-design/references/source-examples.md): the video's flight, note, mood-board, and event patterns, plus the book's broader principles.
- [Review guide](skills/layered-grid-design/references/review.md): inspect relationships and correct observed failures.

The skill is model-neutral and can be used with GPT-6 Astra. Its folder is self-contained; copy the entire `skills/layered-grid-design` folder into your authoring environment's supported skills directory to install it. Brand fonts, source artwork, the book PDF, and the reference video are not bundled. Supply those separately when a task requires them.

## Scope and provenance

This repository distinguishes verified brand rules, proposed working defaults, and unresolved gaps. Adding a composition skill does not make its optional numerical presets official Databricks standards. See [implementation notes](implementation-notes.html) for this integration's decisions and checks.
