# Technical Approach

## Objective

Build a retrofit-friendly evacuation intelligence layer that can transition from simulation to hardware-assisted deployment.

## Core Pipeline

1. Input acquisition (simulated now; real sensors planned)
2. Local preprocessing and signal conditioning
3. Zone-level risk computation
4. Building graph update
5. Dynamic shortest-safe-path simulation (Dijkstra)
6. Guidance presentation via dashboard and sign previews

## Why Dijkstra (Current Stage)

- Interpretable behavior for judges/reviewers
- Fast enough for local simulated decisions
- Easy to encode weighted penalties for risked zones

## Risk Modeling (Demonstration Scope)

- **Safe:** no active hazard influence
- **Caution:** traversable with elevated penalty
- **Blocked:** route excluded where possible

## Offline-First Principle

- Maintain local decision ability even if external network is unavailable
- Prefer local caching and deterministic fallback behavior

## Planned Evolution

- Integrate real-time sensor streams from ESP32 nodes
- Add TinyML anomaly scoring
- Introduce gateway-level fusion and confidence weighting
- Evaluate heuristic + probabilistic routing extensions
