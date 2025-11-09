# RPS Strategy Analyzer

A Python project to simulate and analyze different strategies in the classic Rock-Paper-Scissors (RPS) game. The project implements a variety of strategies, including probabilistic, reactive, and adaptive behaviors, and allows comparisons between them through simulation.

## Features

* **Multiple Strategies**:

  * `s_random`: Choose R, P, or S with equal probability.
  * `s_constant`: Always pick the same move (R, P, or S).
  * `s_main_choice` / `s_neglected_choice`: Probabilistic bias toward a preferred move.
  * `s_mimic_opponent`: Repeat opponent’s last move.
  * `s_tend_to_repeat` / `s_tend_to_change` / `s_never_repeat`: Adapt based on previous choices.
  * `s_result_dependent`: Repeat or change move depending on previous round outcome.
  * `s_human_like`: Probabilistic strategy that favors certain moves and adapts slightly to previous results.

* **Simulation Engine**: Play two strategies against each other for a given number of rounds.

* **Statistics**: Automatically calculates win/loss/tie percentages.

## Requirements

* Python 3.8+
* `numpy`

Install dependencies:

```bash
pip install numpy
```

(`random` is part of the standard library and does not need installation.)

## Insights from Simulations

Simulation results and insights are maintained in the notebook. For example:

* `s_human_like` tends to outperform simple constant strategies but is mostly balanced against `s_random` or other adaptive strategies.
* Games against `s_mimic_opponent` result in fewer ties, even if win rates are similar.

Future analysis will include theoretical exploration using **Algorithmic Game Theory**.

## Optional Improvements and Future Work

* **RPS Strategy Analyzer**: Analyze real game data from two players (past rounds) to detect patterns, potentially using ML or DL algorithms.
* **More Adaptive Strategies**: Implement strategies that consider longer histories, probabilities, or patterns — not just the last move — for smarter decision-making.
* **Visualization Tools**: Add plots to show win/loss/tie trends, strategy effectiveness, and tie dynamics.
* **Tournament Mode**: Allow multiple strategies to compete in a round-robin tournament to rank their effectiveness.
* **Interactive Tool**: Package as a command-line tool or small web app for interactive experiments.
