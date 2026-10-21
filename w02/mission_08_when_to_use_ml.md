# Mission 8 — Does this problem need ML?

## Example: deciding when to cool an electronic system

**Goal:** avoid overheating while minimising pump energy. **Success criteria:** safe operating temperature, low energy use, and acceptable false alarms.

| Aspect | Fixed rule | Possible ML approach |
|---|---|---|
| Decision | Turn pump on at or above a specified temperature | Predict near-future overheating from temperature, power and ambient conditions |
| Data | Current temperature, calibrated sensor | Historical time-series measurements and known outcomes |
| Strength | Simple, transparent, cheap to validate | Can adapt to multiple interacting signals |
| Weakness | May switch unnecessarily or respond late | May mispredict under unfamiliar conditions |
| Failure | Bad sensor or poorly chosen threshold | Data drift, biased data, false negative prediction |
| Evaluation | Over-temperature events and pump energy | Same measures plus recall, false alarms, model latency |

**Decision:** Start with a rule-based baseline. Only add ML if it demonstrably improves safety/energy trade-offs on independent data. Keep a hard safety cutoff even if ML is used. For high-consequence cases, human oversight and robust fallback rules matter. A dataset alone does not justify ML.
