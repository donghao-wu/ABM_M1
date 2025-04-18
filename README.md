# Donghao(Lucius) Wu Midterm Exercise 1 Sugarscape Model Modification

# Sugarscape with Class-Based Agent Behavior

This is a modified version of the classic **Sugarscape** agent-based model built using the [Mesa](https://mesa.readthedocs.io/) framework. The original model simulates agents harvesting sugar on a spatial grid, with behavior driven by vision and metabolism. This version introduces **social class dynamics** and movement preferences based on emergent inequality.

## Model Features

- Agents collect sugar to survive.
- Each agent has:
  - A metabolism rate
  - A vision range
  - A current sugar endowment
- Sugar regenerates on the grid at each step.

## Modification: Class-Aware Agent Movement

This model introduces a **social stratification system**:
- Agents are assigned to **classes** (`low`, `middle`, `high`) based on their average sugar over time.
- **High-class agents** avoid moving near low-class agents when selecting their next position.
- **Class mobility** is allowed — agents can move up or down based on their sugar history.
- (Optional) Low-class agents can request aid from richer neighbors.

This modification adds a layer of **social preference and inequality feedback** to the model.

## GUI Interface

The GUI displays:
- Agents as colored dots (blue = low, orange = middle, red = high)
- Sugar levels on the grid (yellow intensity)
- A dynamic **Gini coefficient plot** showing wealth inequality over time.

## How to Run

`solara run app.py`
