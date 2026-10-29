---
name: forecast-lifecycle
description: Implement or review immutable forecasts, abstention evaluation, calibration, experiences and improvement experiments.
---
# Forecast lifecycle
Version: 1.1, 2026-10-29. Reconstructed reference procedure.

## Procedure
1. Read domain, forecasting and memory KB plus current STATUS.
2. Define precise outcome, horizon, evaluation schedule, reference state and applicable scoring before the outcome is known.
3. Insert an immutable forecast containing information cutoff, evidence snapshot and model/prompt/feature/strategy versions. Revisions create new linked versions.
4. Record trade/wait/reject and reason. Abstention preserves the forecast and does not remove evaluation.
5. Evaluate matured forecasts only with available outcome data. Separate probability/distribution quality, execution, costs and portfolio effects. Report calibration/cohorts, horizon and sample size; one probabilistic miss is not automatic model failure.
6. Label counterfactual trades SIMULATED. Specify feasible entry/exit, spread, fees, slippage and fill assumptions; a missed move is not proven profit.
7. Store experience with original belief, outcome, attribution and evidence-linked lesson. Do not replace original evidence with reflection text.
8. Keep memory improvements, calibration, strategy versions and model/code experiments distinct. Log all attempted experiments; require out-of-sample baseline comparisons and rollback before promotion.

## Acceptance
Tests demonstrate immutable originals, new-version revisions, evaluated abstentions, no future leakage, correctly timed labels and no silent candidate deployment. Preserve simple baseline results. Report actual commands/output/revision/environment and unresolved evaluation contamination limits.
