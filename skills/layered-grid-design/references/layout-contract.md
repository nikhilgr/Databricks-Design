# Layout contract

Use a compact contract to prevent independent decisions from drifting. Adapt the fields to the deliverable; this is a working design record, not a required user-facing YAML artifact. Attribute each resolved value to an existing rule, a proposed default, or an intentional exception.

| Decision | Record |
|---|---|
| Purpose | Audience, primary message, reading order, intended action |
| Output | Medium, canvas/viewport, native units, expected viewing size, export constraints |
| Authority | Applicable design-system file/template and relevant component rules |
| Frame | Outer margins, safe areas, crop/bleed constraints, column count, gutters |
| Rhythm | Base spacing scale, selected tokens, justified substeps |
| Groups | Component boundaries, insets, within-group gaps, between-group gaps |
| Structure | Column spans, image aspect ratios, anchors, intentional negative space |
| Typography | Role → family, size/unit, weight, leading, measure; per-component scope |
| Behavior | Stacking, wrapping, overflow strategy, content growth, format variants |
| Exceptions | Value, reason, affected scope; do not call a proposal an official token |
| Verification | Rendered cases and measurements, remaining limitations |

## Concrete brand-system binding

Suppose a supplied brand file specifies DM Sans and DM Mono, approved colors, but explicitly omits spacing and radius rules:

- Preserve the specified fonts and palette. Do not introduce Inter/Baskerville just because the source example uses them.
- Propose spacing geometry appropriate to the requested medium and mark it as provisional.
- Do not interpret an omitted radius field as either zero radius or permission to claim that 24px is official.
- Prefer the existing asset template where it specifies margins or component shapes.
- Use the layered method regardless of whether the final result uses rounded containers.

## Example compact UI proposal

For a new 352px-wide card with no governing component tokens:

- Proposed spacing unit 8px; outer radius 24px; inset 24px.
- Available content width: 352 − 2×24 = 304px.
- Two equal columns with an 8px gutter: (304 − 8) / 2 = 148px.
- A 16px gap between the image group and its caption; an 8px gap between related image tiles.
- Image tiles use their own appropriate inner radius; it need not equal the outer radius.
- Content determines height. The source video's 352px mood-board height is not evidence for this proposed card width.

These dimensions are a worked example, not a universal component specification.

## Carry the contract into generation

A usable prompt supplies content and relationships, not just adjectives:

> Use the attached design system for identity and established tokens. Apply the resolved layout contract. Build the frame, safe areas, content groups, and type hierarchy before polish. Add another component using the same contract. Render the required sizes, report material exceptions, and fix clipping or hierarchy problems.

When another task or tool needs a source, attach or supply the source explicitly. A local filename in a prompt does not guarantee that the other environment can access it.
