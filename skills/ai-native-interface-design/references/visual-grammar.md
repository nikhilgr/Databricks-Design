# Visual grammar

These are observations from Beautiful UI and proposed adaptations, not universal design rules. Source paths and commit are in source-audit.md.

## What to preserve

**Information hierarchy before decoration.** A neutral stage contains a raised surface; a quieter inset contains code, evidence or a chart. Text has primary, secondary and tertiary roles. A compact summary opens into detail without competing with the result. Use accent for focus or an important action; semantic colors describe state.

**Optical consistency.** Upstream uses Inter plus JetBrains Mono, a 14px body base, tight tracking, 12px card padding, 10×12px bars/table padding, and radii of 6/8/10/14px for chips/controls/cards/windows. These are observed source values. Adopt the relationship between scales; use the host brand and raise text size for presentation media. Tiny demo labels are not a readability target.

**Elevation carries meaning.** Start with a solid hairline for contained evidence; add a restrained layered shadow for a floating card; reserve the strongest elevation for an overlay. Dark mode needs new surface/border/ink values, not a global inversion. Do not put every paragraph in its own elevated card.

**Motion follows state.** Upstream examples use opacity and small translations, strong ease-out curves, gliding menu highlights, and measured-height expansion. Recommended starting ranges: 100–160ms hover/focus, 180–280ms reveal, 280–400ms panel expansion. These are adjustable design defaults, not product requirements. Keep the result stable after completion. Pause autoplay when a person engages. A reduced-motion mode must stop JavaScript-driven sequencing as well as CSS animation.

## Default composition choices

| Need | Preferred shape | Avoid |
|---|---|---|
| Single answer | Plain answer with an embedded evidence surface | A dashboard grid for one question |
| Inspect result | Answer on left; optional evidence pane on right | All panes permanently open |
| Dense rows | Real table, sticky header, constrained horizontal scroll | Shrinking columns until unreadable |
| A choice | Short question, meaningful options, visible selection | Decorative chips with ambiguous selected state |
| A claim | Finding, time window, units, evidence reference | Floating percentage with no denominator |
| Marketing hero | One large outcome and one cropped focal component | An entire desktop scaled to postage-stamp text |

Use generous space around the focal object and compact spacing inside it. Keep one clear alignment axis. Distinguish clickable chips from metadata with semantics, focus and affordance, not color alone. Keep numerical columns right-aligned and tabular, narrative text left-aligned, code monospaced.

## Original token starter

assets/tokens.css is a scoped, dependency-free proposal with neutral light/dark values and a Databricks concept override. It is not a byte-for-byte extraction. Import it only in a new concept or map its roles onto existing tokens. Components remain responsible for layout, accessible controls, and complete states. Do not replace a host app's global theme.

Normal text should meet 4.5:1 contrast; large text and essential non-text controls should meet 3:1. Check actual foreground/background pairings after applying overrides. Tertiary ink is for secondary information, never disabled-looking essential instructions. Keep chart series identifiable with labels or line styles as well as color.
