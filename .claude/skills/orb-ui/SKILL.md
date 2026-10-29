---
name: orb-ui
description: Build or review the MNS living graph, real-event stream, orb panels, decision trace and historical playback.
---
# Orb interface
Version: 1.1, 2026-10-29. Reconstructed reference procedure.

## Procedure
1. Read orb UI, architecture/domain KB and current STATUS.
2. Map every node, edge and pulse to a stored record or real event with IDs, timestamps and trace linkage. No fake analytical activity or invented internal thoughts.
3. Define visual encoding for type, status, freshness, running task and unresolved forecast. Separate probability, source reliability and evidence completeness.
4. Use the accepted React/TypeScript + 3d-force-graph design unless an ADR changes it. Provide searchable list/2D fallback, focused neighbourhoods, filters and level-of-detail.
5. Panels expose state, changes, evidence/provenance, forecasts, decisions, evaluations and recorded lessons.
6. Trade view answers why now, decisive evidence, disagreement, strategy version, invalidation, actual fills and subsequent outcome.
7. Historical playback enforces as_of; present-day summaries cannot leak into past views. Animation coalescing is acceptable when traceable.
8. Test event provenance, reconnect handling, filtering, readable non-colour cues and representative graph/update loads.

## Acceptance
Visible activity resolves to actual events; fixture demos are labelled; no mocked activity appears live. Measure graph size, update rate and UI latency rather than promise scale. Report exact checks/output/revision/environment.
