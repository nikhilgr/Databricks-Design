# Databricks Design

A design framework for creating Databricks components, presentations, documents, and marketing assets with AI-assisted authoring.

## Design resources

| Resource | Responsibility |
| --- | --- |
| [design.md](design.md) | Databricks visual identity, typography, colors, logo rules, component guidance, and documented source gaps |
| [AI-Native Interface Design skill](skills/ai-native-interface-design/SKILL.md) | AI component patterns, interactive artifacts, creatives, images, and demo-video workflows, with an optional Databricks Genie profile |
| [Layered Grid Design skill](skills/layered-grid-design/SKILL.md) | Composition through spacing rhythm, safe areas, content groups, structure, and typography, followed by rendered review |

Use the design system with the skill relevant to the task. Layered Grid Design guides composition; AI-Native Interface Design guides AI interaction patterns and their translation across media. Established brand rules and supplied templates take precedence over either skill’s optional defaults.

## Build an asset

Give the authoring assistant the brief, audience, content, output dimensions, relevant brand assets or template, and the relevant resources above. In Codex, use `$layered-grid-design` when the skill is installed; otherwise point the assistant directly to its SKILL.md.

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

## AI-native interfaces and Genie

Use `$ai-native-interface-design` when installed, or point the assistant to [its SKILL.md](skills/ai-native-interface-design/SKILL.md). Copy the complete folder to install it. The generalized skill includes an optional Genie profile informed by this repository’s brand context.

> Use $ai-native-interface-design and design.md to build a responsive Databricks Genie revenue-analysis concept with a chart, expandable SQL, and useful follow-up questions. Use the bundled illustrative fixture and label the output as concept UI with sample data.

Included resources:

- [Component atlas](skills/ai-native-interface-design/references/component-patterns.md): 21 Beautiful UI patterns and their adaptations.
- [Implementation guidance](skills/ai-native-interface-design/references/implementation.md): controlled states, real streaming, approval payloads, and source-specific pitfalls.
- [Media workflows](skills/ai-native-interface-design/references/media-translation.md): artifacts, creatives, images, and rendered demo videos.
- [Genie profile](skills/ai-native-interface-design/references/databricks-genie.md): brand context, product scope, and evidence/verification semantics.
- [Source audit](skills/ai-native-interface-design/references/source-audit.md): immutable repository links and research limitations.
- [Illustrative fixture](skills/ai-native-interface-design/assets/genie-revenue-scenario.json): consistent revenue values, SQL, and a 20-second timeline.

The bundled CSS is a proposed concept starter, not official Genie product tokens. The fixture is fictional. Storyboard guidance does not itself provide a rendered video. No upstream component library, commercial icons, brand fonts, or artwork are bundled.
