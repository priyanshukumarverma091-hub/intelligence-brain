Intelligence Brain

A rule-based query understanding and multi-agent routing engine. Given a natural-language query, IntelligenceBrain detects intent, extracts entities/requirements/constraints, scores complexity, and recommends which specialized agents (Coding, Data Analysis, ML, Research, Reasoning, Critic) should handle the task.

Features
Intent detection — classifies queries into MACHINE_LEARNING, DATA_ANALYSIS, CODING, RESEARCH, REASONING, or GENERAL.
Entity extraction — recognizes known tools/frameworks/languages (Python, TensorFlow, pandas, SQL, etc.).
Requirement extraction — implementation, optimization, analysis, explanation, debugging, research, comparison, prediction.
Complexity & confidence scoring — numeric scores (0–1) used to decide whether multiple agents / external tools are needed.
Agent routing — maps understanding to a de-duplicated list of recommended agents.
Requirements
Python 3.7+
No third-party dependencies (uses only dataclasses, typing, re from the standard library).
Usage
python
from brain import IntelligenceBrain, print_decision

brain = IntelligenceBrain()
decision = brain.think("build a machine learning model and improve its accuracy")
print_decision(decision)

Run the built-in test suite directly:

bash
python brain.py
Project Structure
.
├── brain.py         # Core IntelligenceBrain implementation + test suite
├── README.md
├── requirements.txt
└── LICENSE
License

MIT — see LICENSE.
