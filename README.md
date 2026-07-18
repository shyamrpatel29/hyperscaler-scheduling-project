# Hyperscaler Scheduling MIP

A draw-tower scheduling case: one production line, three hyperscale customers (Meta, NVIDIA, Amazon), each wanting the line dedicated to their spec for the quarter. Only one customer can be loaded at a time, and switching specs costs both money and downtime.

Solved as a mixed-integer program with Gurobi to pick which customer to dedicate the line to and how many units to produce, maximizing quarterly profit under capacity, demand, and changeover constraints.

The notebook also stress-tests the MIP's answer with a Monte Carlo simulation over historical demand variability, and a discrete-event simulation (SimPy) to check utilization and queueing behavior against the optimization result.

All figures in the case are made up for practice, not real numbers.

## Contents

- `hyperscaler_scheduling_MIP.ipynb` — model formulation, solve, sensitivity checks, Monte Carlo simulation, and discrete-event simulation

## Tools

Python, Gurobi (gurobipy), NumPy, Matplotlib, SimPy
