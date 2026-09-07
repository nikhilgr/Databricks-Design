# Adapt the method to the medium

Read the section for the current deliverable. The 8px/24px recipe describes compact screen components; the underlying relationships transfer more widely than those numbers.

## Web and product components

Use existing component and spacing tokens before adding new ones. A 4px system can express an 8px primary rhythm without changing its foundation. Make padding, gaps, and type roles reusable variables where the framework supports them.

Use fluid columns with explicit gutters. Let content drive height. Test the relevant narrow and wide viewports, long headings, error/empty states, and larger text. Maintain semantic reading order when visual spans change. Do not reduce readable type simply to preserve a desktop arrangement on a phone.

Distinguish a square spacing overlay from a baseline overlay. Browser line boxes, fonts, borders, and fractional layout can produce geometry that does not land on every square-grid intersection.

## Slides and carousels

Begin with the real template and canvas. Define recurring headline, content, page-marker, and optional footer zones; use the brand's logo exclusion area independently. Keep slide-to-slide anchors stable while letting content shape the composition.

Express dimensions in the authoring tool's native units. If converting a logical design canvas, document the mapping: a 1600-unit-wide layout mapped onto a 13⅓-inch-wide slide uses 120 layout units per inch; a 72-unit margin becomes 0.6 inches. This is an example mapping, not a default slide template or a command to use 8pt spacing.

Evaluate text at presentation or feed size, not just on the editor's large artboard. A three-role type hierarchy can scale up for a keynote slide. Separate dense evidence into another slide before making it illegible. Preserve necessary disclosures and source labels.

For social carousel exports, inspect the platform's actual target dimensions and crop behavior when relevant. Keep content away from known crops and interface overlays; do not invent universal platform-safe-area measurements.

## Marketing images, ads, and campaign families

Choose one primary message, its proof or image, and an appropriate action. A shared grid does not require a card wrapper. Allow oversized type, asymmetrical spans, and intentional open space while preserving meaningful alignment.

Set geometry at the target composition size, then inspect at its expected displayed size. Do not assume that 24 source-image pixels have the same visual effect as 24 CSS pixels in a small component.

Adapt each aspect ratio deliberately. Preserve focal point and message order; recompose rather than stretch or blindly crop. Anchor logos according to brand clear-space requirements, not the generic inset token.

Keep imagery and claims grounded in the brief. When image generation is appropriate, specify composition and reserved copy areas, then use precise authoring tools for final typography where fidelity matters. A generated image's apparent grid is not evidence of exact spacing.

## Documents and reports

Use native paragraph styles, margins, columns, and spacing controls. Build hierarchy with semantic headings, body, captions, tables, and notes. Define a baseline or leading rhythm where it helps sustained reading; do not impose an 8px square grid on running text.

Choose measure and leading together. Check long tables, figures, page breaks, captions, widows/orphans, and footnotes in rendered pages. A report may need more than three document-wide sizes while still keeping each recurring component restrained.

Avoid translating a document into a stack of decorative cards. Let continuous text, tables, figures, and whitespace serve the reading task.

## Print and large-format work

Use the required physical dimensions, trim, bleed, and viewing distance. Treat print margins and logo clear space separately from component insets. Translate the modular rhythm into suitable native units; type-size decisions depend on reading distance and format.

Confirm production constraints from supplied specifications or an authoritative current source when needed. Do not invent bleed or color-management requirements from the screen-component recipe.
