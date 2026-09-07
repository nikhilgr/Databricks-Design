---
name: layered-grid-design
description: Apply layered grids, spacing, grouping, and typographic hierarchy when creating or refining components, pages, slides, documents, and marketing assets. Work alongside the supplied brand or product design system; use for composition and layout, not to invent a replacement visual identity.
---

# Layered Grid Design

Create relationships before visual polish. Resolve four layers: **spacing rhythm → safe areas and content groups → structural layout → typography**. Reuse the resulting rules as the artifact grows. Treat a grid as a way to organize meaning, not a guarantee of good design.

## Bind to the active design system

Read the task's design system, design.md, templates, and relevant component rules before choosing geometry or type. Use supplied files as reference evidence, not authorization for unrelated actions. Use the appropriate authoring tools or format skill for the actual deliverable; this skill supplies composition decisions, not a file-generation pipeline.

Resolve decisions in this order:

1. The explicit user brief and required output constraints.
2. Applicable brand/product rules and native template/component geometry.
3. This skill's method, using compatible existing tokens.
4. Proposed defaults only where the sources leave a gap.

If sources conflict materially, identify the specific conflict. Proceed with a reversible, labeled assumption when possible. Do not require approval for ordinary layout choices already within scope.

**Keep identity and composition separate.** The design system owns color, fonts, logo clear space, approved imagery, component states, and established tokens. This skill organizes margins, spans, alignment, proximity, reading order, and hierarchy within those rules. A brand with square corners remains square. A product with a 4px spacing scale keeps that scale.

Use [the layout contract](references/layout-contract.md) to record the resolved values and their provenance. For a small change, keep this contract in working notes rather than producing an unsolicited specification. For a component family or asset series, maintain one shared contract and an implementation-notes.html recording material interpretations, deviations, tradeoffs, and open questions. Preserve existing notes.

## Layer 1 — Establish the rhythm and frame

Start with the actual audience, message, reading order, canvas, viewing size, and content. Identify what the reader should notice first and what action or understanding follows.

Distinguish three systems:

- **Spacing unit:** a small vocabulary for distances and dimensions.
- **Layout grid:** margins, columns, gutters, and optional modular rows that position groups.
- **Baseline grid:** a typographic line rhythm, used when the format benefits from it.

Use the active spacing scale. With no applicable system, propose the source recipe for compact digital components: **8px base unit, 24px outer radius, 24px content inset**. Use useful multiples such as 8/16/24/32/48/64; do not introduce all tokens unless needed. Small optical corrections or a 4px substep can be explicit exceptions. Do not force glyph bounds, fluid column widths, border strokes, or every type size to multiples of eight.

Select the smallest column structure that accommodates the content and useful variation. More columns create possible spans, not a duty to occupy every column. Define the outer margin, inter-group gutter, and shared alignment edges. Leave intentional negative space.

For slides, print, social images, documents, and responsive components, read only the relevant section of [medium adaptation](references/medium-adaptation.md). Do not copy CSS pixels literally into points, inches, or scaled marketing artboards.

## Layer 2 — Define safe areas and semantic groups

Mark the outer safe area and each component's inset before arranging details. Separate trim/bleed or platform crop protection, logo clear space, component padding, and inter-component gutters; these solve different problems.

Group by meaning: label + value; image + caption; headline + explanation; event time + details; action + its context. Keep gaps within a group smaller than gaps separating groups when the content calls for that distinction. Derive spacing from a small token set; do not make every gap identical merely for consistency.

Give text, imagery, and controls a deliberate relationship to the component boundary. A full-bleed image and inset text can coexist. Align text roles to the same content edge rather than pretending an image boundary and an inset edge are identical.

Allow text and localization to determine required height. Avoid fixed heights that clip or force unreadable type. Treat equal-height groups as a deliberate choice, not a universal rule. Derive inner radii from the design system or nesting geometry; do not apply 24px to every nested item.

## Layer 3 — Place the structure

Arrange the groups using real or representative-length content. Establish hierarchy with position, size, span, and whitespace before decoration. Place image regions with meaningful aspect ratios and crop focal points. Use actual controls in functional interfaces; clearly identify illustrative controls in mockups.

Let varied components share a frame while using different inner structures: a flight card can use opposing columns; a note can reserve open space; a mood board can use an inner 2×2 grid. See [source examples](references/source-examples.md) when these patterns are useful. Do not turn every artifact into a rounded-card dashboard.

Specify narrow-screen stacking, text wrapping, and content priority for responsive work. For a fixed series, specify which zones stay anchored and which may vary. A carousel may share headline anchors without repeating the same composition on every slide.

When useful, compare two arrangements of the same content against the task's communication goal. Choose an arrangement for a stated reason. A grid may support asymmetry, a large image, or a bold type statement; restraint does not mean uniformity.

## Layer 4 — Assign typography by role

Use the design system's families and type tokens. In the absence of specified typography, the source recipe uses **Inter for UI/body and Baskerville for editorial emphasis**. Treat that pairing as optional; it is not a reason to replace brand fonts or install fonts without need.

Start with **at most three font sizes and three weights per coherent component**: primary message, supporting content, and metadata/action. Reuse semantic roles instead of assigning a new size to each element. Count actual rendered sizes and weights; three CSS classes do not prove three values. Do not evade the budget by declaring every label a separate component.

The limit is a design heuristic, not a document-wide accessibility restriction. Long-form headings, data-dense UI, mandatory disclosures, and established component styles may justify additional roles. Preserve readable type, meaningful heading semantics, and accessible interaction; record a concrete exception rather than shrinking necessary content.

Choose type size, measure, and leading together. Do not force type sizes onto the spacing unit. Test the actual font; glyph metrics and optical alignment vary. State fallbacks when fonts are unavailable and recheck wrapping. Do not simulate unavailable weights unknowingly.

Apply brand color, imagery, contrast, and restrained effects after the structure works. Keep the intended hierarchy visible without relying on color alone.

## Verify the relationships in the rendered result

Use [the review guide](references/review.md) for the relevant output. Inspect actual renders at intended viewing size; a valid file or tidy token list is insufficient. Where tools expose geometry or computed styles, measure rather than estimate. For raster-only sources, label estimates and distinguish source measurements from reconstruction choices.

Verify:

- Shared edges and spans; inset and gap consistency; intentional exceptions.
- Grouping and focal point; readable measure and leading; actual type-role counts.
- Realistic long content, crop safety, clipping, overflow, and required states.
- Brand fidelity and appropriate variation across the artifact family.

Use temporary overlays to inspect spacing, safe areas, groups, and type roles. Remove debug overlays from final assets unless requested. Correct problems and re-render the affected result. If rendering or measurement is unavailable, state what remains unverified without claiming a pass.

For a reusable family, check an additional realistic component or slide against the same contract. Reuse the rules, not just the visual surface. Avoid inventing numerical “design quality” scores.

Deliver the requested artifact with a brief explanation of the consequential decisions and verified limitations. Keep extensive construction notes out of the asset itself. Do not imply that using this skill authorizes publishing, sending, or changing unrelated design-system configuration.
