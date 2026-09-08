# Component selection atlas

Source files below are under `components/primitives/` at the audited commit. “Transfer” is this skill's design interpretation. Catalog coverage is complete; source audit depth varies by component.

| Source | Useful transfer | Adaptation before real use |
|---|---|---|
| LoadingState.tsx | Small activity mark + meaningful status + elapsed time | Actual busy state; no fabricated progress percentage |
| ThinkingState.tsx | Collapsed operation summary with inspectable steps | Backend events, not timers or invented internal thoughts |
| StreamingText.tsx | Answer with adjacent citations and follow-ups | Actual stream, stable citations, exact source count, no looping |
| ApprovalCard.tsx | One concise clarification at a time | Return selected values AND custom text; explicit commit for consequential actions |
| ToolChips.tsx | Compact operations expanding into results | Stable event IDs; verified status/results instead of timed steps |
| TaskRows.tsx | Parallel or sequential tasks with per-row status | Make each status controlled; explicit failure/retry, no simulated recovery |
| ChatComposer.tsx | Contextual chat with a visible draft | Connect sending/pending/error and preserve drafts |
| PromptBar.tsx | Intent entry plus selected context | Only expose available attachments/models/voice; autocomplete keyboard behavior |
| RecommendationCard.tsx | Suggested action with alternatives and rationale | Evidence-based labels; real action acknowledgement, not local accepted state |
| ContextCards.tsx | Evidence excerpts with identifiable origin | Link authorized provenance; do not expose inaccessible data |
| DiffTable.tsx | Review additions/removals before application | Explicit change set and server response; prototype contains domain-specific rows |
| RecordsTable.tsx | Dense result inspection, sort, resize, selection | Replace CRM-specific columns and calculations; keyboard/touch selection |
| FilterTable.tsx | Visible filters with counts and orderly updates | Counts from actual filtered rows; clear filters/empty state |
| SidebarNav.tsx | Stable conversation/context navigation | Host information architecture and icon licensing; avoid irrelevant upgrade controls |
| SearchList.tsx | Search suggestions and useful no-match state | Keyboard navigation, scope, accessible result count |
| Flowchart.tsx | Explain relationships or ordered work | Edges must reflect real semantics; not evidence of executable orchestration |
| InsightCards.tsx | Headline finding, compact plot, related next question | Real timestamps and samples, units/time range; no synthetic interpolation as facts |
| CodeBlock.tsx | Inspectable, copyable query or diff | SQL-aware rendering or safe plain text; copy raw query only |
| FineTuneCard.tsx | Compact inspector for editable properties | For artifact editing; not an invented Genie configuration panel |
| SelectionActions.tsx | Act on a selected passage with a small toolbar | Keyboard alternative, selection preservation, authentic edit result |
| AgentScreen.tsx | Expand a preview while retaining context | Upstream is an image/viewer with a recording state, not a video recorder |

## A reusable contract

Use the fields the component actually needs, for example:

```ts
type ViewState = 'idle' | 'running' | 'partial' | 'success' |
  'empty' | 'error' | 'cancelled' | 'needs-input' | 'access-denied';
type Evidence = {
  id: string; label: string; href?: string;
  retrievedAt?: string; queryId?: string;
  verification?: { kind: string; detail: string };
};
type ResultView = {
  id: string; state: ViewState; question: string;
  answer?: string; evidence: Evidence[];
  columns?: { key: string; label: string; unit?: string }[];
  rows?: Record<string, string | number | null>[];
  actions: { id: string; label: string; enabled: boolean }[];
  error?: { message: string; retryable: boolean };
};
```

This is a suggested presentation model, not the Genie API schema. Keep transport events and UI state separate. Numeric confidence is optional and should usually be absent. Do not collapse verification, query completion, access authorization and data freshness into one green badge.

## Four composition recipes

- **Analytical answer:** prompt → compact query status → finding → chart/table → inspect query/sources → follow-up. Make the finding primary for business users and evidence accessible for technical users.
- **Proposed edit:** user intent → before/after diff → selected changes → explicit apply → acknowledgement/error. Preserve the old state until success.
- **Research answer:** question → observable retrieval activity → cited synthesis → source excerpts → refinement. Each citation refers to actual evidence, not decorative source logos.
- **Creative editor:** selected object → compact inspector or selection toolbar → preview → undo/accept. Keep the source object stable while controls change.
