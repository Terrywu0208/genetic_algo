# Genetic Algorithm for Flowshop Makespan Problem

## Introduction
This repository contains an implementation of the Genetic Algorithm to solve the Flowshop Permutation problem, a classic problem in scheduling theory. The objective of this project is to minimize the makespan, which is the time required to complete all jobs. For more information about genetic algorithms and the flowshop makespan problem refer to the next section.

## Genetic Algorithm
A genetic algorithm (GA) is a heuristic optimization technique inspired by the evolutionary principles of natural selection and genetics. The algorithm explores the solution search space through selection, mutation, and crossover operations to generate better solutions iteratively. The key principle behind GA is that it imitates the process of natural selection in order to evolve candidate solutions toward optimized ones.

## Flowshop Makespan Problem
The flowshop makespan problem is a well-known problem in scheduling theory that involves a finite set of jobs processing consecutively over a finite number of machines maintaining the same order of processing on every machine. There are m machines and n jobs that have to follow a particular sequence to get processed optimally. Finding the optimal sequence of processing jobs with minimum makespan is known as the flowshop makespan problem. Solving this NP-hard problem exactly requires a significant amount of computational resources. Hence, several heuristic-based methods are used to find near-optimal solutions in polynomial time.

This Jupyter notebook provides a python implementation of GA to solve the flowshop makespan problem. It consists of two main parts:

## Data Preprocessing
This part defines the input data format and parses the data to use it in the GA process.

## Genetic Algorithm Process
This part uses the parameters obtained in data preprocessing step to apply genetic algorithm by using proper encoding schemes, fitness functions, selection, crossover, mutation, population size, gene size, and various hyper-parameters.
Running the Notebook

To run this notebook on your system, you can install these dependencies by running the command
``` pip install -r requirements.txt```

Furthermore, you can open this jupyter notebook in Google Colab or any other notebook service provider.

## References:
https://www.sciencedirect.com/topics/computer-science/flow-shop-scheduling
https://towardsdatascience.com/introduction-to-genetic-algorithms-including-example-code-e396e98d8bf3
https://en.wikipedia.org/wiki/Flow_shop_scheduling