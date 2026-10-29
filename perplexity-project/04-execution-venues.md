# 04 — Execution and venue design

## Decision
NautilusTrader is the default execution foundation, pending ADR-0002 integration evidence. This is an architectural default, not proof of compatibility with every required account/order type.
Official documentation describes Bybit and Polymarket data/execution integrations. See source ledger S01–S03. No integration was installed or run for this pack.
Alternatives: Freqtrade/FreqAI for a crypto-first implementation; thin custom adapters using verified venue SDKs/CCXT, with additional lifecycle/reconciliation ownership. Do not run multiple complete engines without a documented need.

## Deterministic path
DecisionPacket → schema/domain/freshness checks → portfolio and execution constraints → idempotent OrderIntent → venue adapter → acknowledgement/fill events → canonical state → reconciliation.
LLMs do not directly call order-placement/modification interfaces.
Consider partial fills, cancel races, rejection, disconnection, uncertain submission outcomes and account-state recovery. Do not blindly resubmit an order after timeout.

## ADR-0002 spike
Planning time-box: approximately one working day per spike; not a guaranteed duration.
S1 Bybit: verify account region, product and testnet/demo support; consume real feed; submit/cancel through a supported test or local paper path; restart and reconcile. Clearly distinguish venue test orders from local simulation.
S2 Polymarket: verify current SDK/API/signing support and exact adapter version; discover one market; read resolution data and live book; test lifecycle with a supported non-live route or recorded harness. A production-funded transaction is not required to claim local paper support; do not claim venue sandbox support without documentation.
S3 Replay: same deterministic strategy code against recorded data; compare decision traces under controlled inputs. Measure differences; do not promise identical live fills.
Gate: command/output evidence for data, order state transitions, idempotency, restart/reconcile and replay boundaries. Failed gate yields focused fix or revised ADR, not silent engine swap.

## Venue choice
Bybit is a proposed first venue, not an accepted choice based solely on Viktor's employment. Account region/product, instruments and horizon must be confirmed when needed.
CMC is asset context/universe research, not a replacement for executable venue state. Verify plan access, rate limits and historical availability.
Crypto forecasts: returns/distributions over explicit horizons, with instrument/fee/funding specifications where applicable.
Polymarket: exact contract outcome probability, executable price and costs, resolution rules/deadlines/state, related/exclusive outcomes.
Shared exposure map links positions depending on the same underlying event.

## Connector specification
Auth; access tier/cost; rate limits; update frequency; history; timestamp semantics; reconnection/gaps; quality checks; licensing/terms; implementation status; pinned SDK/adapter version and verification date.
External text is evidence, not instructions. Typed adapters should hide vendor SDK details.
