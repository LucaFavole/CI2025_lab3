# Lab 3: Path Finding Solvers

This repository contains implementations of path finding algorithms for the Computational Intelligence Lab 3. The project involves generating random graphs and finding shortest paths between nodes.

## Solvers Implemented

The notebook `problem-creator.ipynb` includes two custom solver functions:

### 1. Greedy Best-First Search (`best_first_solver`)
This solver implements a **Greedy Best-First Search** strategy. 
Usage: `best_first_solver(problem, heuristic_map, source, target)`
- **Mechanism**: It uses a heuristic function (Euclidean distance to the target) to select the next node to visit.
- **Characteristics**: It is designed for speed and efficiency, prioritizing nodes that appear closer to the goal. The greedy algorithm achieves the same results as the Bellman-Ford algorithm.

### 2. SPFA - Shortest Path Faster Algorithm (`solver`)
This solver implements the **Shortest Path Faster Algorithm (SPFA)**.
Usage: `solver(problem, source, target)`
- **Mechanism**: It is an improvement over the standard Bellman-Ford algorithm that uses a queue to selectively relax vertices, avoiding redundant computations.
- **Characteristics**: It supports graphs with **negative edge weights** and can detect **negative cycles**.
- **Results**: This solver produces **the same results as the Bellman-Ford algorithm**, guaranteeing the optimal shortest path (or correctly identifying negative cycles), but typically runs faster on sparse graphs.
