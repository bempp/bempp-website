---
title: Tutorials & example applications
---

A number of Jupyter notebook of example applications are included in the Bempp-cl [GitHub repository](https://github.com/bempp/bempp-cl/tree/main/examples).
They can also be viewed online by following the links below.

## Laplace
### [Solving a Laplace problem with Dirichlet boundary conditions](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/laplace/laplace_interior_dirichlet.ipynb)
This tutorial demonstrates how Bempp can be used to solve a simple Laplace problem,
including plotting a 2D slice of the solution, and will be well suited to new Bempp users.

### [Solving a mixed Neumann-Dirichlet problem](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/laplace/mixed_neumann_dirichlet.ipynb)
This tutorial demonstrates how problem can be solved using finite element space defined on subsets of the boundary.
It includes a demonstration of how functions can be exported in Gmsh and VTK format. 

### [Computing the capacity of a cube with a re-entrant corner](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/laplace/reentrant_cube_capacity.ipynb)
This tutorial demonstrates a practical application of Bempp to calculate the capacity of an isolated conductor.

### [Weakly imposing a Dirichlet boundary condition](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/laplace/dirichlet_weak_imposition.ipynb)
This tutorial demonstrated how Bempp can be used to weakly impose boundary conditions, as proposed in
[<em>Boundary Element Methods with Weakly Imposed Boundary Conditions</em> (2019)](../publications.md#Betcke2019).

## Helmholtz
### [Scattering from a sphere using a combined direct formulation](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/helmholtz/helmholtz_combined_exterior.ipynb)
This tutorial demonstrates an application of Bempp to Helmholtz wave scattering, including the use
of Helmholtz operators and plotting of a 2D slice of the solution.

### [BEM-BEM Coupling using a simple multitrace formulation](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/helmholtz/bem_bem_multitrace_coupling.ipynb)
This tutorial demonstrates a use of Bempp to solve a domain decomposition problem, including the use
of blocked operators.

### [Simple FEM-BEM coupling with FEniCSx for the Helmholtz equation](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/helmholtz/simple_helmholtz_fem_bem_coupling_dolfinx.ipynb)
This tutorial demonstrates how Bempp can be used in combination with [FEniCSx](https://fenicsproject.org/)
(the latest version of FEniCS) to solve a FEM-BEM coupled problem.

### [Simple FEM-BEM coupling with FEniCS for the Helmholtz equation](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/helmholtz/simple_helmholtz_fem_bem_coupling_dolfin.ipynb)
This tutorial demonstrates how Bempp can be used in combination with [FEniCS](https://fenicsproject.org/)
(an older version of FEniCS) to solve a FEM-BEM coupled problem.

### [The OSRC preconditioner for high-frequency scattering](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/helmholtz/osrc_burton_miller.ipynb)
This tutorial demonstrates how an OSRC (on-surface radiation condition) preconditioner can be used for Helmholtz problems.

## Maxwell
### [Electromagnetic scattering from flat screens](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/maxwell/maxwell_screen.ipynb)
This tutorial demonstrates an application of Bempp to Maxwell wave scattering from a screen,
including the use of Maxwell operators and plotting of a 2D slice of the solution.

### [Bistatic RCS generated by dielectric spheres](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/maxwell/maxwell_dielectric.ipynb)
This tutorial demonstrates and example application of Bempp to find a radar cross section generated by a
plane wave scattering from two spheres.

## Other
### [Running performance benchmarks with OpenCL on CPUs and GPUs](https://nbviewer.jupyter.org/github/bempp/bempp-cl/blob/notebooks/other/opencl_benchmark.ipynb)
This tutorial demonstrates the use of Bempp on CPU and GPU devices, and demonstrates some performance results.
