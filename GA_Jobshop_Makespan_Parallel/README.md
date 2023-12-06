# Genetic Algorithm for Job Shop Scheduling with GPU Parallelization

### Overview

This project implements a parallelized genetic algorithm for solving the Job Shop Scheduling (JSS) problem. The JSS problem is a classic optimization challenge in manufacturing, where a set of jobs needs to be scheduled on a set of machines, considering constraints such as processing times and machine availability. The genetic algorithm is used to evolve a population of schedules over multiple iterations, aiming to find an optimal or near-optimal solution.

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

### GPU Parallelization

This implementation utilizes GPU parallelization to accelerate the genetic algorithm's execution. Parallelization involves breaking down the problem into smaller tasks that can be solved simultaneously by multiple processing units on the GPU. This can significantly speed up the optimization process, especially for large-scale problems.

### Main Code (GPU Parallel)

The main code snippet provided focuses on the GPU-parallelized execution of the genetic algorithm. The key steps include:

1. **Initialization**: Generating an initial population of schedules.

2. **Evolution**: Iteratively evolving the population through crossover, repairment, mutation, and fitness evaluation.

3. **Result Output**: Printing the optimal sequence and makespan, as well as visualizing the makespan over generations using a plot.

4. **Gantt Chart**: Generating a Gantt chart to visualize the optimal schedule for jobs on machines.

### Results and Visualization

The project outputs the optimal sequence, optimal makespan, and a Gantt chart illustrating the optimal schedule. Additionally, a plot shows the progression of makespan values over generations, providing insights into the algorithm's convergence.

### Dependencies

- NumPy
- Matplotlib
- Pandas
- Plotly
- GPU with CUDA support (for parallelization)

### Usage

1. Ensure the required dependencies are installed.
2. Execute the provided code snippet.
3. Review the optimal sequence, makespan, and visualizations.
