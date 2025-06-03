# GBO (Gooseneck Barnacle Optimization Algorithm)
# Python Implementation (You can also request MATLAB Implementation)

This repository provides a standalone Python implementation of the Gooseneck Barnacle Optimization (GBO) algorithm, a nature-inspired metaheuristic developed based on the reproductive behaviors of stalked barnacles. GBO is designed to solve complex optimization problems involving continuous, nonlinear, and multimodal functions.

## 🔍 Description

GBO simulates the unique mating strategies of gooseneck barnacles, including:
- Sperm casting across water columns (long-range reproduction),
- Self-fertilization (pseudo-copulation),
- Movement influenced by wave height (exploration),
- Reproductive selection based on fitness-driven mating allocation (exploitation).

This Python implementation can be easily integrated with machine learning or engineering optimization tasks.

## 📌 Features

- Modular and readable Python class for GBO
- Compatible with any user-defined objective function
- Easy integration with machine learning hyperparameter tuning
- Supports boundary constraints and real-coded variables

# Citation Request 

If you use this implementation in your research or publication, please cite the following paper:

- LaTeX:

```bibtex
 @article{ahmed2023gooseneck,
  title={Gooseneck Barnacle Optimization Algorithm: A Novel Nature-Inspired Metaheuristic},
  author={Ahmed, Marzia and Sulaiman, Mohd Herwan and Mohamad, Ahmad Johari},
  journal={Mathematics and Computers in Simulation},
  year={2023},
  publisher={Elsevier},
  doi={10.1016/j.matcom.2023.07.012}
}
```

- APA:
  
Marzia Ahmed, Mohd Herwan Sulaiman, Ahmad Johari Mohamad, “Gooseneck Barnacle Optimization Algorithm: A Novel Nature-Inspired Metaheuristic,” Mathematics and Computers in Simulation, Elsevier, 2023. https://doi.org/10.1016/j.matcom.2023.07.012

** File Structure**
GBO_Original.ipynb — Python class implementing the GBO algorithm
example_usage.py — Sample script for testing GBO
README.md — Documentation and citation
requirements.txt — Package dependencies

# Contributing

There are lots of ways how you can contribute to Permetrics's development, and you are welcome to join in! For example, 
you can report problems or make feature requests on the [issues](/issues) pages. 

Developed by: [Dr. Marzia Ahmed](mailto:ahmed.marzia32@gmail.com?Subject=GBO_QUESTIONS) @ 2024



## 🧪 Example Usage

```python
def objective_function(x):
    # Example: Sphere function
    return sum(x**2)

optimizer = GooseneckBarnacleOptimizer(
    obj_func=objective_function,
    lb=[-10]*5, ub=[10]*5,
    dim=5, pop_size=20, max_iter=100
)

best_solution, best_fitness = optimizer.optimize()
print("Best solution:", best_solution)
print("Best fitness:", best_fitness)

## Alternative:
if __name__ == "__main__":
    pop_size = 30
    dimensions = 10
    lb = -10  # lower bound
    ub = 10   # upper bound
    max_iter = 100

    best_position, best_fitness = GBO(objective_function, pop_size, dimensions, lb, ub, max_iter)

    print("Best solution found:")
    print("Position:", best_position)
    print("Fitness:", best_fitness)
...

