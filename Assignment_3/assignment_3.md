
# Assignment 3: Python Wrapper Test Case

## Overview
This assignment demonstrates how to incorporate a Python wrapper into a SU2-based CFD simulation. The wrapper dynamically updates boundary conditions for an unsteady flat plate, allowing the wall temperature to change over time. By doing so, we can simulate a more realistic transient heat transfer scenario and observe its effects on flow variables.

## Configuration Updates
- **Solver Setup**: The solver is configured for a RANS simulation with the SST turbulence model.  
- **Unsteady Analysis**: The time-dependent nature of the flat plate’s temperature requires an unsteady solution setup.  
- **Python Script Reference**: Within the `.cfg` file, the relevant boundary condition is linked to a Python script. This script calculates and updates the wall temperature at each time step, ensuring a seamless interaction between the solver and the external code.

## Code Modifications
- **Python Wrapper**: A Python script is used to compute the transient wall temperature:
  ```python
  WallTemp = 293.0 + 257.0 * sin(pi * 0.5 * time)
  ```
  This line updates the boundary condition based on the current simulation time.
- **Boundary Condition Update**: At each iteration, the solver reads the new temperature value from the Python script and applies it to the flat plate. This allows the solver to capture the resulting changes in the flow and temperature fields.

## Rebuild Process

## Visualization with ParaView
- **Sample Time Steps**: Typical snapshots (e.g., at t=0.11111, t=0.33333, t=0.66666, and t=0.99999).
![temp_1](./assig_3_images/temp_1.jpg)
![temp_2](./assig_3_images/temp_2.jpg)
![temp_3](./assig_3_images/temp_3.jpg)
![temp_4](./assig_3_images/temp_4.jpg)