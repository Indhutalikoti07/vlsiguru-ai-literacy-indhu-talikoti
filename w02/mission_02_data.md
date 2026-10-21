# Mission 2 — Understand data

A **dataset** is a collection of examples. Each row is a **sample** or observation; a **feature** is an input measurement; a **label/target** is the desired answer. Learning a pattern means finding a relationship that can be useful on new examples, not memorising each row.

## Synthetic chip timing dataset

These values are invented for illustration, **not actual measurements or training results**.

| Run | Clock target (ns) | Logic depth | Fanout | Congestion (%) | Timing result |
|---|---:|---:|---:|---:|---|
| R1 | 2.0 | 12 | 4 | 35 | Pass |
| R2 | 1.2 | 18 | 8 | 72 | Fail |
| R3 | 1.8 | 14 | 5 | 42 | Pass |
| R4 | 1.0 | 21 | 9 | 81 | Fail |
| R5 | 1.5 | 16 | 6 | 55 | Pass |
| R6 | 1.1 | 19 | 7 | 76 | Fail |

**Features:** clock target, logic depth, fanout, congestion. **Target:** timing pass/fail. The run ID is an identifier, not a useful predictive feature. The label is categorical; the other inputs are numerical. A table is structured data, while free-text timing reports and layout images are less structured.

**Labelled vs unlabelled:** With the timing result column, the table supports supervised learning; without it, grouping similar runs could be an unsupervised exercise.

## Data collection and quality

Collect representative runs across designs, constraints and process corners. Check units, duplicate runs, inconsistent naming and invalid sensor readings. Missing values might require investigation, careful imputation, or excluding unusable rows. Noisy observations may come from measurement variation; labels can be wrong if the timing report was misinterpreted.

Two ways quality hurts: (1) wrong pass/fail labels teach an incorrect relationship; (2) collecting only easy, uncongested designs makes predictions unreliable for congested designs. More rows do not fix systematic bias. Use only public or synthetic data for this assignment. [S1, S3]
