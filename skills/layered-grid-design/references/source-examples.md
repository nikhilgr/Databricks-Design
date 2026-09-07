# Source method and reusable examples

## Attribution and evidence boundary

The user supplied an explanation attributed to @MSchwaibold, associated with https://x.com/MSchwaibold/status/2096059496812716307?s=20, plus the local video `5RVH4OvhQyJbrtkV.mp4`.

The explanation supplies the layered workflow, an 8px base grid, 24px radius and inset, Inter/Baskerville, and a ceiling of three font sizes and three weights per component. The website was inaccessible during the original review; the supplied video provided direct visual evidence later. Do not describe these choices as universal standards or as measurements from CSS.

The silent video lasts 27.55 seconds. It shows a collection of cards and individual cards alongside a square grid and inset band. The reference frames below were visually inspected. The source media is not bundled into this portable skill; these descriptions are sufficient to apply the patterns. Request the actual media only when close visual reproduction requires it.

## Four patterns

| Source frame | Observed structure | Transferable decision |
|---|---|---|
| Flight, 20.30s | SFO and JFK at opposing edges; cities and times repeat those edges; route line connects groups | Use paired columns for related endpoints. Align related metadata with its endpoint. |
| Quick note, 22.60s | Small label, larger serif thought, lower yellow status badge with open space above it | Give the primary thought priority; separate metadata with whitespace rather than extra decoration. |
| Mood board, 11.50s | Four image tiles in a 2×2 group; caption at left and count at right below | Use a nested grid and smaller internal gutters to make varied images read as a collection. |
| Upcoming event, 12.20s | Prominent time; title/duration group; bottom row of avatars and directions | Group information by when, what, and who/how; establish a clear first focal point. |

The video labels 24px radii, a 352px mood-board height, and a 240px event height at the cited frames. Flight/note height labels vary during transitions, including 238px and 241px. Do not turn transitional measurements into fixed tokens. Sample font sizes, card widths, and colors in the companion tutorial were reconstruction choices.

## The broader grid principle

The supplied scan of Josef Müller-Brockmann's *Grid systems in graphic design* informed the method through focused visual reading:

- PDF p. 7 / printed p. 11: modular fields, shared dimensions, and separation between fields.
- PDF p. 25 / printed p. 30: column width, type size, and leading work together; excessively short and long lines both introduce reading effort.
- PDF p. 50 / printed p. 57: choose the grid after studying the task; subdivisions create options and tradeoffs.

The scan had no extractable text on its opening pages. These references describe a focused reading, not a complete OCR analysis. The exact modern UI values and font pairing come from the user-supplied explanation, not from the book.
