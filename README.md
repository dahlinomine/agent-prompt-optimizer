# Agent Prompt Optimizer

![optimization](https://img.shields.io/badge/optimization-blue?style=flat-square) ![genetics](https://img.shields.io/badge/genetics-blue?style=flat-square) ![prompts](https://img.shields.io/badge/prompts-blue?style=flat-square)

Uses genetic algorithms to evolve agent prompts for specific benchmarks.

## Overview
Agent Prompt Optimizer is a Python-based framework designed to systematically improve LLM performance through evolutionary computation. By treating prompts as genotypes, the system automatically iterates through variations—mutating and recombining instructions—to discover the optimal configuration for a given scoring benchmark.

## Features
*   **Evolutionary Engine:** Implements mutation, crossover, and selection processes to explore the prompt space.
*   **Benchmark Integration:** Evaluates candidate prompts against user-defined metrics and datasets.
*   **Population Management:** Maintains a diverse pool of high-performing prompts to avoid local optima.
*   **Extensible Architecture:** Easily swap out LLM providers or define custom fitness functions.

## Installation
Ensure you have Python 3.8+ installed. Clone the repository and install the dependencies:

```bash
git clone https://github.com/yourusername/agent-prompt-optimizer.git
cd agent-prompt-optimizer
pip install -r requirements.txt
```

## Usage
Configure your initial prompt and benchmark settings in the configuration file, then run the optimization loop:

```bash
python main.py --config configs/default.yaml
```

**Example:**
To evolve a prompt for a creative writing task:
```python
# main.py internally initializes the optimizer
optimizer.run(
    initial_prompt="Write a concise summary.",
    generations=10,
    population_size=20
)
```
The system will output the highest-scoring prompt after the final generation.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change. Ensure that your code adheres to the existing style and passes all local tests.

## License
This project is licensed under the [MIT License](LICENSE).