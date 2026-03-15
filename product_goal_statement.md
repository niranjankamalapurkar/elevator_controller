# Product Goal Statement

## Vision
To design and validate a Safety-Critical Motion Control System for vertical transit. The primary objective is to demonstrate a rigorous Systems Engineering lifecycle—from concept to validation—prioritizing deterministic passenger safety, human-centric comfort (UX), and fault-tolerant architecture.

This project serves as a technical demonstration of architectural decomposition, formal requirement tracing, and "Safety-by-Design" principles commonly found in Autonomous Vehicle (AV) and ADAS domains.

## Development Roadmap: Build Level 0 (Baseline)
The "Minimum Viable Controller" focuses on the Single-Car Vertical Transit Baseline.

### Level 0 Goals
- Basic Mission Profile: Receive a destination, calculate direction, execute motion, and verify arrival.
- Create state machine for basic mission profile
- Define and enforce 'Safe State' transitions.

### Assumptions
- Simplified Environment: Single car, fixed floor heights, no "hall calls" (only internal car buttons).
- Deterministic Timing: Control loop runs at a fixed frequency (e.g., 100Hz).
- Digital I/O: Sensors are treated as boolean flags (e.g., Floor_2_Reached = TRUE).
