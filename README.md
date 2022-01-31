# RBF-PHS for Incompressible Flow with application to a Couette Flow

__This code was written by Anand Radhakrishnan__

This code solves for an incompressible Couette flow between two cylinders, with the inner one rotating at a constant angular speed. 
The theoretical formulation is in the `JCP_Paper.pdf` paper in the root directory.

Mesh files `.msh` in `conc_circle_geoms/` were generated with `gmsh`.
The code has 4 main components:
1. Operator discretization for pressure Poisson with all Neumann boundary conditions in `Grid.cpp`
2. Multigrid preconditioned GMRES/ ILU-GMRES solvers in `FracStepMultirid.cpp`
3. Fractional Step procedure in `fractionalStepGrid.cpp`
4. Main file which generates the simulation in `FractionalStepSim.cpp`

Build using `make all`
