# Bias Evolution in Multi-Agent Debate

## Overview
Studying Convergence Dynamics in Biased NLP Agents
A research-oriented NLP project exploring how training bias influences the convergence behavior of multi-agent debate systems.
This project builds a Proposer–Critic debate framework where two sentiment analysis agents trained with different bias levels iteratively debate over predictions until they reach convergence.
Instead of simply predicting sentiment, the system analyzes:
1. how bias affects disagreement
2. how agents resolve conflicts
3. how long debates take to stabilize

The goal is to study stability, convergence, and accuracy in biased multi-agent reasoning systems.

## Motivation
Understanding bias is crucial in multi-agent systems as they can affect outcomes in various applications including negotiations, collaborative filtering, and automated decision-making.

## Research Objectives
1. To analyze how biases manifest and evolve in multi-agent debates.
2. To develop frameworks and models that can mitigate bias impacts.
3. To evaluate the effectiveness of these models in real-world scenarios.

## Dataset
The project uses the **IMDb Large Movie Review Dataset**.

Dataset details:

* 50,000 movie reviews
* Balanced sentiment dataset
* Binary classification:
  * Positive
  * Negative

Dataset split used in this project:

| Split | Size |
| ----- | ---- |
| Train | 80%  |
| Test  | 20%  |

The test set remains **fixed across all experiments** to ensure fair comparisons.

## System Architecture
The system consists of two agents:
    1. Proposer Agent: The proposer provides the initial sentiment prediction.
    2. Critic Agent: The critic evaluates the proposer’s prediction and provides a counter-argument.

The agents debate iteratively until their predictions converge.

## Multi-Agent Debate Flow
1. Agents initiate a debate with predefined biases.
2. Interaction sequences trigger exchanges of arguments and counterarguments.
3. Agents update their opinions based on the discussions.

## Bias Injection Framework
To simulate bias, training datasets are intentionally skewed.

We define a bias parameter β:

β ∈ {0.0, 0.1, 0.2, ..., 1.0}
Bias Level	Dataset Distribution
0.0	50% positive / 50% negative
0.5	75% positive / 25% negative
1.0	100% positive

For each bias level:

Proposer is trained with bias β

Critic is trained with opposite bias

This forces the agents to disagree systematically.
## Convergence Rule
A convergence rule defines how agents settle on opinions based on their debate interactions, promoting consensus or highlighting disagreements.

## Experimental Pipeline
1. Data collection and preprocessing.
2. Agent training with bias frameworks.
3. Execution of multi-agent debates.
4. Analysis of outcomes based on defined metrics.

## Evaluation Metrics
- Bias score
- Consensus level
- Argument quality
- Outcome effectiveness

## Expected Results
- Insights into how biases evolve.
- Effective frameworks for bias mitigation.
- Recommendations for system designs in multi-agent settings.

## Project Structure
- `/src` - Source code
- `/data` - Datasets
- `/docs` - Documentation
- `/tests` - Test cases

## Installation
Clone the repository and install dependencies using the provided requirements file.

```bash
git clone https://github.com/manasahk28/MultiAgentSystem.git
cd MultiAgentSystem
pip install -r requirements.txt
```

## Requirements
- Python 3.7+
- Necessary Python libraries as listed in `requirements.txt`

## Running Instructions
Execute the main script to start the multi-agent debate simulation.

```bash
python main.py
```

## Visualization Outputs
Visualization modules will generate graphs and interactive outputs to analyze the results of debates.

## Key Contributions
1. Comprehensive analysis of biases in multi-agent systems.
2. Innovative mitigation strategies.
3. Framework for future research in related fields.

## Applications
 - The framework can be extended to:
 - misinformation detection
 - fact verification
 - multi-agent reasoning systems
 - AI safety research
 - bias mitigation studies

## Future Work
Potential improvements include:
 - more than two debating agents
 - argument generation with large language models
 - dynamic debate strategies
 - adaptive confidence weighting
 - multilingual datasets
 - 
## Authors
- Manasa(https://github.com/manasahk28)
