---
name: execution-spike
description: Verify the NautilusTrader default against required venue data, order lifecycle, idempotency, recovery and replay behaviour.
---
# Execution spike
Version: 1.1, 2026-10-29. Reconstructed reference procedure.

## Preconditions
Read ADR-0002, execution/venue KB and STATUS. NautilusTrader is the accepted default pending integration evidence, not an undecided engine. First venue, account region/product and credentials are not inferred.

## Procedure
1. Verify current official adapter/API documentation; pin compatible dependencies and environment. Document supported order types and test routes.
2. S1 Bybit: if configured, consume real data; submit/cancel through a documented venue test route or local paper harness; test duplicate intent, partial-fill/cancel and restart/reconciliation cases.
3. S2 Polymarket: verify market/contract/resolution identity, live book, SDK/signing compatibility and a supported non-live lifecycle harness. Do not assume a venue sandbox exists.
4. S3 Replay: use the same deterministic strategy logic on recorded inputs, compare decision traces and explain boundaries. Live fill equality is not promised.
5. Distinguish acknowledgements, fills, rejection, uncertain submission and account reconciliation. Never blindly resubmit after timeout.
6. Report exact command/output/exit code/revision/environment for each criterion. Blocked checks remain blocked/unverified, not passed.
7. Update ADR gate evidence and STATUS. Failed gate requires a focused fix or proposed ADR revision, not silent engine replacement.

## Acceptance
Evidence covers data, transitions, intent idempotency, recovery and replay boundaries. No live funded transaction is required for the initial gate. Proposed time-box is adjustable, not a completion promise. LLMs never directly execute orders.
