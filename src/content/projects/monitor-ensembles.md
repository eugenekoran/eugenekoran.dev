---
title: "Ensemble Monitoring for AI Control"
description: "Co-authored AI safety research showing that combining diverse LLM monitors detects backdoored agent code more reliably than scaling a single model — presented at AIWILD and AI4GOOD @ ICML 2026."
pubDate: 2026-02-17
tags: ["AI Safety", "AI Control", "Inspect AI", "PyTorch"]
category: research
---

## Overview

Research conducted as part of the Supervised Program for Alignment Research (SPAR), investigating multi-monitor ensemble techniques that enhance the safety-usefulness Pareto frontier for AI Control systems by strategically aggregating diverse monitoring signals.

Presented at the AIWILD and AI4GOOD workshops at ICML 2026.

## Contributions

- Designed the experimentation infrastructure and formulated core research hypotheses
- Ran and analyzed experiments on improving LLM monitoring performance in AI Control setting
- Explored ensemble aggregation strategies to optimally combine monitor outputs

## Results

- Diverse monitor ensembles outperform single monitors — a 3-monitor ensemble achieves **13.1% improvement** over the baseline, vs. only 5.5% from running three copies of the same monitor
- Ensemble gains plateau quickly — a carefully chosen 3-monitor ensemble matches a 12-monitor ensemble at one-quarter the compute cost.
 
## Links

- [Paper (arXiv:2605.15377)](https://arxiv.org/abs/2605.15377) — Ensemble Monitoring for AI Control: Diverse Signals Outweigh More Compute
- [GitHub Repository](https://github.com/Multi-Signal-Control-SPAR/Multi-Signal-Monitoring)

## Technologies

Python, Inspect AI, OpenAI API, PyTorch
