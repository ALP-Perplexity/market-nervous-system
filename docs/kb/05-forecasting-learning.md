# Forecasting and learning

## Forecast lifecycle
Observation → immutable forecast → trade/wait/reject → scheduled evaluation → outcome and attribution → experience → candidate improvement.
Freeze precise outcome, horizon, reference state, probability/distribution, evidence snapshot, information cutoff and model/prompt/feature/strategy versions before outcome.
Abstention reasons: insufficient_evidence, weak_expected_edge, poor_execution_conditions, portfolio_overlap, stale_information, unresolved_disagreement.
A decision may change; its earlier forecast stays immutable and evaluated.

## Evaluation
Score probabilities with appropriate Brier/log-loss and calibration analysis; evaluate return distributions with suitable separately specified metrics. Report by horizon, regime and sample size.
Separate forecasting from execution, costs and portfolio effects. Evaluate repeated forecasts as cohorts; one probabilistic miss is not automatic proof of model failure.
Counterfactual trades are SIMULATED with explicit feasible entry/exit, fees, spread, slippage and fill uncertainty. A missed move is not proven hypothetical profit.

## Four improvement mechanisms
1 Memory: entity resolution, facts, summaries, indexing and expiry.
2 Forecasting: calibration, source reliability, features and regime-specific performance.
3 Strategies: versioned parameters and policies.
4 Code/model research: isolated candidate artifacts and evaluated training changes.
Adding memory is not updating model weights.
Use hypothesis → implementation → experiment → evaluation → promotion/rejection → monitoring, with out-of-sample evaluation, realistic costs, baseline comparison, attempted-experiment registry and rollback.
Start simple: memory + calibration + supervised forecasting; add complexity only if justified.
