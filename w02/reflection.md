# Week 02 — Personal reflection

> **Personalise before submission:** These are example answers to help you reflect; keep only statements that describe what you actually learned.

## What is clearer now?

I can better separate a learning paradigm from a task type. For example, supervised learning describes learning from known answers, while classification describes predicting a category. I also understand why high accuracy does not guarantee that a model detects rare failures.

## What still confuses me?

I would like to understand more clearly how reinforcement-learning rewards are designed and how researchers confirm that a placement improvement remains useful after routing and timing analysis.

## What would I like to learn next?

I want to explore neural networks, model training, and how ML could assist VLSI physical design and verification without replacing engineering signoff.

## How I verified my work

I checked the distinctions among learning paradigms against IBM's ML overview, reviewed leakage and evaluation concepts in scikit-learn documentation, and consulted the original Nature paper and Google Research write-up for the semiconductor case. I have not trained or deployed an ML model for this assignment.

## One example I can explain without notes

In a batch with 95 good chips and 5 defective chips, predicting every chip as good gives 95% accuracy but zero defect recall. This is why defect detection needs recall and a confusion matrix, not accuracy alone.
