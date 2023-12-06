# Genetic Algorithm for Automated Flow Shop Scheduling

This repository contains a Python implementation of a Genetic Algorithm (GA) for solving the Flow Shop Scheduling problem with the objective of minimizing total weighted tardiness. In this problem, there are `n` jobs and `m` machines. The processing order of each job on the machines is the same.

### Problem Description

- Number of Jobs (n): 20
- Processing Times (p): [10, 10, 13, 4, 9, 4, 8, 15, 7, 1, 9, 3, 15, 9, 11, 6, 5, 14, 18, 3]
- Due Dates (d): [50, 38, 49, 12, 20, 105, 73, 45, 6, 64, 15, 6, 92, 43, 78, 21, 15, 50, 150, 99]
- Weights (w): [10, 5, 1, 5, 10, 1, 5, 10, 5, 1, 5, 10, 10, 5, 1, 10, 5, 5, 1, 5]

### Genetic Algorithm (GA)

1. **Algorithm Introduction**:
   - Genetic Algorithm (GA) is an optimization algorithm inspired by biological evolution. In the context of the Flow Shop Scheduling problem, GA uses a population of individuals, where each individual represents an arrangement of jobs. The algorithm iteratively evolves the population using crossover and mutation operations to find an optimal solution that minimizes total weighted tardiness.

2. **Initialization**:
   - Set algorithm parameters such as population size, crossover rate, mutation rate, mutation selection rate, and the number of iterations.
   - Randomly generate an initial population, where each individual represents an arrangement of jobs.

3. **Iterative Evolution**:
   - For the specified number of iterations, repeat the following steps:
      - **Crossover Operation**: Select two individuals as parents from the current population and decide whether to perform crossover based on the crossover rate. Use Partially Matched Crossover (PMX) to generate two offspring.
      - **Mutation Operation**: Mutate the newly generated individuals based on the mutation rate. Use gene displacement for mutation.
      - **Fitness Evaluation**: Calculate the fitness of each individual, which is the reciprocal of the total weighted tardiness. Higher fitness indicates a better individual.
      - **Selection Operation**: Select individuals for the next generation based on fitness.

4. **Result Output**:
   - Output the optimal individual's job arrangement, optimal value (total weighted tardiness time), average tardiness time, and other relevant information.

5. **Gantt Chart Visualization**:
   - Generate a Gantt chart based on the job arrangement of the optimal individual to visually display the scheduling of machines.

### How to Use

1. Clone this repository to your local machine.
2. Open the terminal and navigate to the project directory.
3. Run the script using the following command:

    ```bash
    python flow_shop_scheduling_ga.py
    ```

4. Follow the prompts to input algorithm parameters.
5. The optimal sequence, optimal value, average tardiness, and other information will be displayed, and a Gantt chart will be generated.

### Dependencies

- Python 3.x
- NumPy
- Plotly
- Matplotlib