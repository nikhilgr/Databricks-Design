# Review the rendered design

Verify observable relationships, not compliance theater. Use only checks relevant to the output and available tools. A score cannot substitute for judgment.

## Inspect in four passes

1. **Frame and rhythm:** inspect margins, spans, gutters, and repeated distances. Identify the common content edges. If one element breaks alignment, decide whether the exception is meaningful or accidental.
2. **Grouping:** inspect which objects read together before reading their words. Compare within-group and between-group gaps. Check image/caption and label/value relationships. Distinguish deliberate negative space from an accidental hole.
3. **Hierarchy and reading:** identify the first focal point and intended reading path. Check measure, leading, font fallback, type-role counts, and whether supporting content competes with the primary message. Inspect at intended viewing size.
4. **Behavior and identity:** check long content, cropping, clipping, relevant states and responsive variants. Verify brand fonts, colors, image treatment, logo clear space, and existing component conventions.

For DOM-based work, inspect computed styles and bounds for the relevant components. Count distinct font sizes and weights on visible text, not CSS declarations, icon fonts, or debug annotations. Report any extra role and its purpose. For native slides/documents, inspect actual text styles and object positions where available. For raster work, distinguish visual estimates from source geometry.

## Temporary overlay

Reveal these independently when useful:

- Spacing grid with the unit and origin identified.
- Outer margins, columns/gutters, and component spans.
- Safe-area and inset bands.
- Content-group boundaries and text roles.

Do not obscure the design with all overlays at once unless their relationships are the subject of review. Remove overlays from final exports. A line box fitting an 8px rhythm does not prove the glyph baseline is aligned.

## Correct the actual failure

| Failure | First correction to consider |
|---|---|
| “Everything feels equally important” | Reduce competing emphasis; restore a primary role and regroup supporting material |
| “The grid is consistent but the layout feels dull” | Reconsider spans, focal point, image scale, asymmetry, or negative space; retain useful shared anchors |
| “The card looks cramped” | Inspect content density, inset, measure, and height together; do not simply shrink the type |
| “One card introduces many new sizes” | Map its content to existing semantic roles; add a role only if its meaning requires it |
| “Mobile breaks the composition” | Reflow groups in reading order; check true available width and content growth |
| “The export is technically valid but unreadable” | Render at actual viewing scale and repair density, font substitution, clipping, or contrast |
| “It resembles the reference but violates the brand” | Restore governing tokens and approved imagery; keep the structural relationships |

## Extension check

For a family or series, inspect an additional realistic member that was not the easiest case: a longer headline, fewer images, more metadata, or another aspect ratio. The system succeeds when it accommodates the variation without arbitrary new values or loss of meaning. Do not force the variation into the first component's silhouette.

Record a short evidence note: what was rendered, which dimensions/states were inspected, measurements when available, corrections made, and material gaps. If rendering is unavailable, report an unverified visual review rather than claiming the artifact passed.
