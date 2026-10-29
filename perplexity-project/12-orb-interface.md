# 12 — Living orb interface

## Purpose
Expose real market intelligence and its lineage, not a decorative dashboard. Hundreds of orbs can be meaningful data objects while a small worker pool activates selected neighbourhoods.

## Orb types and activation
Asset: price/liquidity/news change.
Event: new evidence or deadline.
Narrative: changing supporting evidence/attention.
Forecast: evidence change, invalidation or evaluation due.
Strategy: relevant regime/setup.
Experience: retrieved by comparable situation.
Worker: actual scheduled/running task.
Decision: evaluation/synthesis cycle.

## Visual encoding (proposal, to test)
Type → shape/colour; status → border; freshness → explicit age/fade; running task → pulse; evidence flow → highlighted edge; unresolved forecast → badge.
Keep probability, source reliability and evidence completeness separate. Do not use one undefined “confidence” glow for all three.
A pulse has event_id, entity_id, trace_id and timestamp. Animation sampling/coalescing is allowed; visible events must remain traceable, not imply every backend event must render one-for-one.

## Views
3D graph plus searchable 2D/list fallback; asset/event/narrative/strategy clusters; filters, level-of-detail and focused neighbourhoods; contradiction visibility; historical as_of playback.
Detail panel: current state, changes, evidence/provenance, connected forecasts/decisions, evaluations, lessons and active task.
Trade panel: why now, decisive evidence, disagreement, strategy version, invalidation, actual fills, outcome.
Display concise recorded rationale and structured artifacts, not fabricated internal thought.

## Readability and performance
Benchmark actual graph sizes, update rates, draw calls and UI latency. Avoid drawing all history at once. Keep click-through evidence usable, keyboard/list navigation available and status understandable without colour alone.
