# Implementing the patterns

## Prefer adaptation over copying the entire app

Reuse the host framework, token system and icon library. A self-contained HTML/CSS/SVG artifact can express most patterns without new packages. In React, split reusable presentation components from a demo controller and the transport adapter. Give components controlled content/status props, stable IDs and callbacks; keep fixture data out of component bodies.

If copying upstream, inspect its exact imports and required CSS. `:root` variables alone do not define Tailwind utilities: upstream also needs `@theme inline` mappings and component-specific rules. Check path aliases, fonts, utility merging helpers and package dependencies. Registry metadata is not proof of a complete dependency closure. Preserve the MIT notice with copied substantial code; license text is in the repository. Do not copy site analytics, email capture, sounds or development overlays just to obtain components.

Follow project package rules. In this user's Node projects use pnpm, exact versions, package provenance/release-age checks and frozen CI lockfiles. Do not copy upstream floating versions or execute its README installation commands blindly. Prefer existing icons: upstream SidebarNav references a commercial icon library whose license check runs during installation. No external library is essential to the generalized visual approach.

## Source-specific traps

- `atoms/StreamText.tsx`: its effect resets the character count whenever `text` changes. Appending tokens to that prop restarts the reveal. Render accumulated backend text directly or use an append-aware queue with a stable message ID; a demo character animator is not a streaming transport.
- `StreamingText.tsx`: timer-driven word reveal, default looping, a default source label of ten despite three sample sources. Disable demonstration loops and derive source labels from actual evidence. Verify citation association rather than round-robin or decorative placeholder logic.
- `ThinkingState`, `ToolChips`, `TaskRows`: temporal sequences determine some states. Replace these with controlled operation events; do not let failure become success when a timer expires.
- `ApprovalCard.tsx`: stores custom text separately but `onSubmitted` receives only selected indices. The last radio option schedules `send` in a closure that can reference older answers. Model a complete answer payload and submit the current data explicitly. Treat this as a code-reading finding, not a reproduced runtime test.
- `RecommendationCard.tsx`: Accept flips local state. Real acceptance should track submitting, acknowledged and failed states.
- `InsightCards.tsx`: creates timestamps from the current clock and smooths data with Catmull–Rom resampling. Keep historical dates and measured values for analytics; interpolation can overshoot and hover values must not masquerade as recorded samples.
- `CodeBlock.tsx`: its keyword tokenizer targets JavaScript. For SQL, use existing SQL support or escaped plain text. Do not execute displayed code.
- `PromptBar.tsx`: demo animation temporarily patches Math.random for a visual effect. Use explicit seeded data or remove the effect; avoid global random overrides.
- `AgentScreen.tsx`: recording toggles state and an elapsed counter; it does not encode a video. Use an actual capture/rendering tool for MP4 output.
- `scripts/build-registry.mjs`: uses fixed CSS line slices and omits AgentScreen. The complete gallery is not an exact match for published registry items.

## Meaningful verification

Test the primary path and the failure most likely to corrupt user understanding:
1. Append several text chunks: earlier text stays visible, citations stay attached, completion does not loop.
2. Submit a typed clarification and the final selected option: the handler receives their current values once.
3. Fail a query and retry: failure persists until a new result; old results are labeled if retained.
4. Filter/sort: counts, rows, chart and headline remain consistent with the same data scope.
5. Keyboard and narrow layout: controls remain reachable; long SQL scrolls inside its own pane; menus restore focus; selected options have non-color indicators.
6. Reduced motion: stop autoplay, character timers, chart pulses and smooth scroll as appropriate; preserve access to completed information.

Run only tests relevant to what was implemented. For demos, label simulation and use a deterministic replay with a manual restart. Prefer elapsed timeline state to chains of unsynchronized timers when rendering a video. Do not build a fake backend for an image-only request.
