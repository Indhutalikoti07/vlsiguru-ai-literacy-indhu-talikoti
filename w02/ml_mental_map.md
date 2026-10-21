# ML Foundations Map — Final synthesis

## Landscape

```mermaid
flowchart TD
 AI[Artificial intelligence] --> RULES[Rule-based AI]
 AI --> ML[Machine learning]
 ML --> DL[Deep learning]
 AI --> GEN[Generative AI]
 DL -. commonly supports .-> GEN
 GEN --> LLM[Language generation / LLMs]
 ML --> PARA[Learning paradigms: supervised / unsupervised / reinforcement / self-supervised]
 ML --> TASK[Task types: classification / regression / clustering / anomaly detection / reduction / ranking]
```

Learning paradigms specify **where the learning signal comes from**; task types specify **what result the system is expected to produce**.

## Seven-stage lifecycle

```mermaid
flowchart TD
 A[1 Define problem: goal, constraints, success] --> B[2 Understand data: samples, features, labels, quality]
 B --> C[3 Select rule-based or ML approach and task]
 C --> D[4 Prepare data and train on training set]
 D --> E[5 Validate, compare baseline, test generalisation]
 E --> F[6 Deploy for inference and decisions]
 F --> G[7 Monitor drift, errors and human oversight]
 G -->|New data or changed requirements| B
 E -->|Poor metrics or leakage| C
```

**Failure points:** wrong or unrepresentative data at stage 2; leakage or overfitting at stages 4–5; distribution shift and unchecked false negatives at stages 6–7.

**Semiconductor application:** deep RL for chip macro placement. Inputs include netlist and placement constraints; outputs are placement decisions; quality is checked with PPA-related metrics. **Limitation:** improvements in proxy rewards may not transfer to routed timing, new designs or other process nodes. See Mission 9 and [S5–S6].
