# Job Shop Scheduling Problem Solver using Genetic Algorithm in Python

## Introduction

This Python script provides a solution to the Job Shop Scheduling Problem (JSSP) using a genetic algorithm. JSSP is a well-known optimization problem in manufacturing, where a set of jobs must be processed on a set of machines with specified processing times. The objective is to find an optimal schedule that minimizes the makespan, representing the total time required to complete all jobs.

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

## How to Use
1. Prepare an Excel file ("JSP_dataset.xlsx") with two sheets: "Processing Time" and "Machines Sequence."
2. Run the script and input the algorithm parameters when prompted (press Enter to use default values).
3. Review the results, including the optimal sequence, makespan, and Gantt chart.

Feel free to customize the algorithm parameters or integrate it into your workflow for solving Job Shop Scheduling Problems. For more detailed information on each step, refer to the comments in the Python script.