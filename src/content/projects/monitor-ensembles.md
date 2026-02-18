---
title: "Monitor Ensembles for AI Control"
description: "Developed diverse monitor ensembles that outperform scaling a single monitor by 2.4x at detecting backdoored code in AI Control setting."
pubDate: 2026-02-17
tags: ["AI Safety", "AI Control", "Inspect AI", "PyTorch"]
category: research
---

## Overview

Research conducted as part of the Supervised Program for Alignment Research (SPAR), investigating multi-monitor ensemble techniques that enhance the safety-usefulness Pareto frontier for AI Control systems by strategically aggregating diverse monitoring signals.

_Preparing findings for ICLR 2026 submission_

## Contributions

- Designed the experimentation infrastructure and formulated core research hypotheses
- Ran and analyzed experiments on improving LLM monitoring performance in AI Control setting
- Explored ensemble aggregation strategies to optimally combine monitor outputs

## Results

- Diverse monitor ensembles outperform single monitors — a 3-monitor ensemble achieves **13.1% improvement** over the baseline, vs. only 5.5% from running three copies of the same monitor
- Gains are largest exactly where it matters: **31% better recall at 1% FPR**, the strictest operational threshold
 
## Links

- [GitHub Repository](https://github.com/Multi-Signal-Control-SPAR/Multi-Signal-Monitoring)

## Technologies

Python, Inspect AI, OpenAI API, PyTorch
