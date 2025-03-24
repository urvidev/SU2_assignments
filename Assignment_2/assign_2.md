# Assignment 2: 2D Axisymmetric Turbulent Jet

## Overview
In this assignment, a 2D axisymmetric mesh was generated (using tools such as Gmsh) to simulate a steady-state turbulent jet. The objective was to set up a SU2 configuration, run the solver, and examine results like velocity and temperature distributions. The test case provides a foundation for understanding mixing phenomena and serves as a reference for comparing numerical predictions with published experimental data.

## Configuration Updates
- **Solver Selection**: RANS (Reynolds-Averaged Navier–Stokes) approach with the SST (Shear Stress Transport) turbulence model.  
- **Axisymmetric Setup**: The computational domain is set as a 2D axisymmetric problem to capture jet flow development along the axis.  
- **Boundary Conditions**:  
  - **Inlet**:  
    - Total Temperature: 302.4 K  
    - Total Pressure: 118,309.784 N/m²  
    - Velocity Direction (x): 100.0 m/s  
  - **Outlet**:  
    - Back Pressure: 115,056.0 N/m²  
- **Mesh**: A structured or unstructured 2D grid (revolved around the axis) defines the jet inlet region and downstream flow field. Proper refinement ensures accurate resolution of the jet shear layer.  
- **Solver Parameters**: Time-steady formulation, with iteration limits and convergence criteria set to capture the flow physics without temporal evolution.

## Rebuild Process

## Visualization with ParaView
![velocity](./assig_2_images/velocity.jpg)