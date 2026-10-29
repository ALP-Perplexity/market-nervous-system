# ADR-0002 — Execution foundation
Date: 2026-10-29.
Status: NautilusTrader ACCEPTED DEFAULT; integration acceptance PENDING SPIKE.

## Decision and rationale
Use one event-driven foundation for crypto and prediction markets if required adapter
behaviour passes the gate. Official docs describe Bybit and Polymarket integrations:
https://nautilustrader.io/docs/latest/integrations/bybit/
https://nautilustrader.io/docs/latest/integrations/polymarket/
Documentation is not proof of our account/order/product compatibility.

## Alternatives
Freqtrade/FreqAI: faster crypto-first path, separate prediction-market integration likely.
Thin custom using verified SDKs/CCXT: more control, more lifecycle/recovery code to own.

## Spike
S1: verify Bybit region/product/version and test route; real data; submit/cancel
through supported local paper or venue test path; restart/reconcile; duplicate intent test.
S2: Polymarket discovery, resolution semantics and live book; verify SDK/signing/version;
exercise non-live lifecycle through supported simulation/recorded harness.
S3: recorded-data replay with same deterministic strategy logic and controlled inputs.
Planning time-box: approximately one day per spike, adjustable based on findings.
Do not require live funded trades for the initial gate. Never claim a venue sandbox
exists unless official documentation confirms it.

## Acceptance evidence
Exact commands/output/revision/environment, pinned dependencies, data provenance,
order state transitions, partial-fill/cancel/recovery cases, idempotency and replay boundaries.
Live fill equality is not expected or promised.

## Consequences
Learning curve/adapter/version work. If criteria fail: report, propose focused fix or
revised ADR. Do not silently switch engines or declare skipped tests passing.
