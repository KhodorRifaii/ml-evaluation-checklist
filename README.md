# ML Evaluation Checklist

A short, practical checklist for evaluating machine learning and LLM systems before they ship.

## How to use it
Copy the checklist into your project's pull request template or release notes, and tick each item before you release. Items that don't apply can be removed, but write down why.

## Data
- [ ] Split train/validation/test by time or entity when leakage is possible
- [ ] Check label quality on a sample you label by hand
- [ ] Record data source, date range and known gaps

## Metrics
- [ ] Pick one primary metric that matches the business goal
- [ ] Report a baseline (majority class, simple rule or last model)
- [ ] Report uncertainty (confidence interval or repeated runs)

## LLM and RAG systems
- [ ] Build a fixed eval set of real questions with expected answers
- [ ] Check retrieval separately from generation (did the right chunk come back?)
- [ ] Test in the languages users actually use
- [ ] Log failures and review them weekly

## Before release
- [ ] Measure latency and memory on the target hardware
- [ ] Add a fallback when the model is unavailable or over quota
- [ ] Write down what the system must not do, and test for it
