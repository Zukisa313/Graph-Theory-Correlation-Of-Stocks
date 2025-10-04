# Numerical Simulations of Markov Processes

This repository contains Python code for simulating and analyzing two fundamental types of Markov processes: the **Poisson Process** and the **Birth-Death Process**. The simulations are implemented in a Jupyter Notebook and leverage libraries such as NumPy, Matplotlib, and SciPy.

## Concepts Covered

* **Markov Processes**: Systems that transition between states based only on their current state, not their past history.
* **Poisson Process**: A counting process that models the number of events occurring in a fixed interval of time, where events happen at a constant average rate.
* **Birth-Death Process**: A special case of a continuous-time Markov process where state transitions are only between neighboring states (births increasing the state by one, deaths decreasing it by one).
* **Discretized-Time Simulation**: An approximation method where time is advanced in small, fixed steps (`dt`), and the probability of an event in each step is calculated.
* **Random-Jump-Time Method (Gillespie Algorithm)**: An exact simulation method where the waiting time to the next event is drawn from an exponential distribution. This is generally more efficient and accurate than the discretized-time method.
* **Absorbing States & Absorption Time**: Analysis of states that, once entered, cannot be left. This includes calculating the probability and expected time to reach such a state (extinction).

## Repository Contents

* `Markov_Simulations.ipynb`: The main Jupyter Notebook containing the Python code, explanations, and plots for all simulations.
* `README.md`: This file, providing an overview of the project.

## Requirements

To run the notebook, you will need the following Python libraries:
* `numpy`
* `matplotlib`
* `scipy`

You can install them using pip:
```bash
pip install numpy matplotlib scipy
```

## How to Run

1.  Clone this repository to your local machine.
2.  Ensure you have the required libraries installed.
3.  Open and run the `Markov_Simulations.ipynb` notebook in a Jupyter environment (like Jupyter Lab or VS Code).

## Summary of Questions Answered

### Question 4: Poisson Process

This section explores a Poisson process $N_t$ with rate $\alpha = 0.5$ and $N_0 = 0$.
* **(a, c)** Simulates and plots 10 trajectories using both the **discretized-time** and **random-jump-time** methods.
* **(b, d)** Computes and plots the histogram of the process value at $t=10$, $N_{10}$, for both methods, comparing the simulation results to the theoretical Poisson distribution.
* **(e)** Provides a qualitative comparison of the two simulation methods, discussing their efficiency and accuracy.

### Question 5: Absorbing State in a Birth-Death Process

This section analyzes a birth-death process $X_t$ with a birth rate $\alpha = 0.5$, a death rate $\beta = 1.0$, and an absorbing state at 0.
* **(a)** Generates 20 trajectories starting from $X_0 = 10$ until they are absorbed at state 0.
* **(b)** Numerically estimates the probability of absorption (extinction) within the time interval $[0, 10]$ for a process starting at $X_0 = 5$.
* **(c)** Estimates the expected time to absorption for a process starting at $X_0 = 10$.
* **(d)** Repeats the estimation for various starting populations ($X_0 = 1, 2, ..., 20$) and plots the relationship between the initial population and the expected time to absorption.
