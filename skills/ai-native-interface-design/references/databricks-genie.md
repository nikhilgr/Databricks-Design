# Optional Databricks Genie profile

Use only when the brief targets Databricks. This profile combines project brand context, public product documentation and proposed interface design. These have different authority.

## Product scope and freshness

Public docs inspected September 7, 2026 Pacific time distinguish Genie Agents (formerly Genie Spaces), Genie One, and Genie Code. Do not apply one surface's features or layout to another. Preserve the user's terminology when appropriate and verify current docs plus an approved screenshot before depicting literal product UI. The default here is a **concept for conversational business-data analysis**, not a replica of an official Genie application.

Primary references:
- [Genie Agents overview](https://docs.databricks.com/aws/en/genie-agents/): domain-specific natural-language analysis returning SQL, tables and visualizations; also distinguishes the Genie family.
- [Genie concepts](https://docs.databricks.com/aws/en/genie-agents/concepts): governed data context, examples, trusted assets, benchmarks and analysis modes.
- [Tune quality / trusted assets](https://docs.databricks.com/gcp/en/genie-agents/tune-quality): trusted queries/functions and relevant verification conditions.
- [Review responses and follow-ups, earlier Spaces documentation](https://docs.databricks.com/aws/en/genie/talk-to-genie): inspect supporting details; trusted matches can still be inappropriate to a question.

Keep verification language literal. A completed query is not a verified answer. Do not invent a confidence score or claim universal accuracy. Use a trusted-asset indication only if the integration actually supplies matching metadata. Do not imply that benchmarks train the agent, or that a UI badge grants access. Show only data and details the user is authorized to see.

## Brand authority

Prefer the user's current design.md/DESIGN.md and approved assets. At creation, this workspace's design.md supplied the following brand context: DM Sans for marketing, DM Mono for code imagery; Lava #FF3621, Navy 900 #0B2026, Navy 800 #1B3139, Oat Light #F9F7F4, Oat Medium #EEEDE9, White #FFFFFF, Gray Text #5A6F77, Gray Lines #DCE0E2. It documents a Navy 900 versus Navy 800 source conflict and provisionally uses Navy 900. This profile preserves that limitation.

Sources for refresh: [brand overview](https://brand.databricks.com/), [extended colors](https://brandguides.brandfolder.com/databricks-extended-brand-guidelines/colors), [typography](https://brandguides.brandfolder.com/databricks-extended-brand-guidelines/typography). No official Genie spacing, radius or motion scale was established. Do not describe this skill's values as official product tokens. Literal captures retain their authentic UI styling; brand typography belongs to editorial framing unless product references confirm it.

Proposed concept mapping: oat background, white result surface, navy primary text/action, gray secondary copy and dividers, lava as a concentrated brand accent. Blue may mark exploration; green may mark a supported success; errors need both explicit text and a distinct treatment. These mappings are recommendations. Lava on white is roughly 3.62:1, so avoid small lava body text and white small labels on lava; a navy CTA with white text is a safer baseline. Recheck each actual pair.

## Core analytical story

1. Establish the selected domain/context and a business question.
2. Show a short observable operation summary if supported; otherwise a neutral busy state.
3. Lead with a direct finding and its scope, date range and units.
4. Pair it with a result table or appropriate chart. Separate association from causation.
5. Offer query/evidence inspection with provenance and any supported trusted-asset metadata.
6. Offer a relevant follow-up that retains filters and context.

Avoid turning the generic model picker, web-search trace, arbitrary file upload, table edits, browser agent viewer or design inspector into alleged built-in Genie features. For a speculative custom app, label these as concept extensions and define their integration separately.

## Portable example

`assets/genie-revenue-scenario.json` is an invented data fixture, not a customer story. It asks for regional revenue comparison between Q2 and Q3 2025. Q2 total is $10.0M; Q3 is $11.8M; change is +18%. EMEA contributes $1.0M of the $1.8M increase (~55.6%). The SQL computes the same periods and fields from a fictional table. There is no trusted-asset verification in this fixture.

Suggested finding: “Revenue grew 18% quarter over quarter. EMEA contributed $1.0M of the $1.8M increase.” Use grouped bars or a regional result table; do not fabricate monthly points from quarterly totals. A relevant follow-up is “Break down EMEA growth by product.” The fixture contains no product breakdown: requesting it should show a clearly simulated/unavailable response or require additional fixture data, not invent a detailed answer.

## Example invocations

- “Use $ai-native-interface-design to build a responsive Genie concept artifact from this revenue CSV, including SQL disclosure and an empty-result state.”
- “Use $ai-native-interface-design with this approved Genie screenshot to create a 1200×628 launch creative. Keep the UI authentic.”
- “Use $ai-native-interface-design to render a 20-second Genie concept demo using the bundled illustrative revenue fixture.”
- “Use $ai-native-interface-design to create an image of an AI answer card for a different brand; do not use the Genie profile.”
