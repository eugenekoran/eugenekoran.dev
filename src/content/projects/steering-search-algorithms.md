---
title: "Steering Search Algorithms"
description: "Developed causal intervention methods to steer Distill-Qwen-1.5B between Depth-First and Breadth-First Search strategies through targeted activation manipulation."
pubDate: 2025-04-18
tags: ["Activation Steering", "Mechanistic Interpretability", "PyTorch"]
---

## Overview

This project explores methods for causally intervening in language model computations to deliberately steer their reasoning strategies. By identifying and manipulating specific activations, we can influence which search algorithms a model employs — in this case, switching between Depth-First Search (DFS) and Breadth-First Search (BFS) on graph traversal tasks.

## Key Contributions

- Applied linear probing across model layers to identify where traversal strategy is encoded
- Developed causal intervention methods for steering model reasoning between DFS and BFS strategies
- Demonstrated targeted activation steering by injecting the DFS/BFS encoding directions via PyTorch hooks

## Links

- [GitHub Repository](https://github.com/eugenekoran/steering-search-algorithms)

## Technologies

Python, PyTorch, Distill-Qwen-1.5B, Linear Probing, Activation Steering
