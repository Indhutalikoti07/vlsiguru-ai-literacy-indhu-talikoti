# Mission 7 — Why ML systems fail

| Hypothetical failure | Likely cause | Evidence to investigate | Mitigation |
|---|---|---|---|
| Timing classifier works on old designs but fails on a new technology node | Distribution shift / unrepresentative training data | Compare node, constraints and feature distributions; measure per-node error | Gather representative new-node examples; monitor and retrain after validation |
| Wafer defect model misses defects under different lighting | Data bias, noise or inconsistent labels | Review false negatives by camera and illumination; audit image labels | Standardise imaging; improve labels; include varied conditions |
| Model scores 99% in testing but fails in deployment | Data leakage, e.g. a feature calculated after final timing signoff | Audit feature availability at prediction time and train/test split by design | Remove leakage features; split by independent designs and time; fit preprocessing on training data only |

Other risks include missing measurements, overfitting, rare failure modes and feedback loops. Human engineers should review uncertain predictions, monitor errors across subgroups, and decide what actions are safe. An incorrect chip-quality prediction may waste testing resources or let faulty hardware pass. [S3]
