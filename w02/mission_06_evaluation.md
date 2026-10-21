# Mission 6 — Evaluation and generalisation

**Training data** fits the model; **validation data** helps choose settings and compare candidates; **test data** provides a final independent estimate. Generalisation means useful performance on unseen cases. **Overfitting** learns training-specific details and performs poorly on new cases; **underfitting** is too simple to capture important patterns. Test data should not guide feature selection or tuning. [S2, S3]

## Worked example: misleading accuracy

Suppose 100 chips include **95 good** and **5 defective** chips. A trivial classifier predicts every chip is good:

| | Predicted defective | Predicted good |
|---|---:|---:|
| Actually defective | 0 (TP) | 5 (FN) |
| Actually good | 0 (FP) | 95 (TN) |

Treat defective as the positive class.

- Accuracy = `(TP + TN) / 100 = (0 + 95)/100 = 95%`.
- Recall for defects = `TP/(TP + FN) = 0/5 = 0%`.
- Precision for defects = `TP/(TP + FP)` = **undefined** because the model never predicts a defect (some software reports zero by convention).

A 95% accuracy model misses **every defect**. Recall is therefore crucial when missing defects is expensive; precision matters when false alarms are costly. A false positive incorrectly flags a good chip; a false negative misses a defective chip. Compare against the majority-class baseline, and inspect a confusion matrix. For numeric regression, mean absolute error measures the average size of numerical mistakes in the target's units. [S4]
