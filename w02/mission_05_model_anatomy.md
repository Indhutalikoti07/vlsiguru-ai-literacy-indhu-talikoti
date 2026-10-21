# Mission 5 — Anatomy of an ML model

An **algorithm** is the procedure used to learn; a **model** is the resulting mapping from inputs to outputs; **parameters** are values learned from data (for example a slope and intercept).

```mermaid
flowchart TD
 A[Training examples: features and targets] --> B[Training algorithm]
 B --> C[Model with parameters]
 C --> D[Predictions on training inputs]
 D --> E[Compare with targets: loss]
 E --> F[Adjust parameters / optimise]
 F --> C
 C --> G[Freeze selected trained model]
 H[New unseen input] --> I[Inference with trained model]
 G --> I
 I --> J[Predicted outcome]
```

**Training** fits parameters using examples. A **loss** describes disagreement between predictions and desired outputs; **optimisation** searches for parameter settings that reduce that loss. **Inference** uses the fitted model on new data without automatically retraining it.

## Linear regression intuition

Imagine estimating delay from logic depth. Linear regression fits a line such as `estimated_delay = intercept + slope × logic_depth` from observed input–delay pairs. The slope and intercept are learned parameters. A new depth is inserted into the fitted equation to estimate delay. A straight-line relationship may be too simple if congestion, wire length and other interactions dominate. [S1, S2]
