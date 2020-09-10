---
title: Changelog
---

## [Bempp-cl 0.2.0](https://github.com/bempp/bempp-cl/releases/tag/v0.2.0)
* In addition to OpenCL all operators are now also implemented in Numba, allowing Bempp to be run on systems without OpenCL stack.
* However, OpenCL is preferrable due to its better performance.
* Internally, the exact implementation of operators has been fully abstracted out so that it is straight forward to write other compute backends (e.g. Cuda, Sycl, etc.)
* All integral operators and potentials can now be assembled via FMM via interfaces to the Exafmm-t library ([github.com/exafmm/exafmm-t](https://github.com/exafmm/exafmm-t)).
* Decorators for grid function callables have been worked over so that it is easy to disable Just-In-Time compilation. Alternatively, a vectorised of grid function callables is now possible.
* The FEniCS interface now allows to obtain trace matrices for Nedelec function spaces for Maxwell FEM/BEM problems.
* Bempp-cl now has automatic deployment with generation of Docker images and a fully automated testing infrastructure.
* Many smaller bug fixes and performance improvements.

## [Bempp-cl 0.1.1](https://github.com/bempp/bempp-cl/releases/tag/v0.1.1)
* Export now works with meshio version 4
* P1 spaces are correctly generated for open domains if `include_boundary_dofs=False`

## [Bempp-cl 0.1.0](https://github.com/bempp/bempp-cl/releases/tag/v0.1.0)
* First release of Bempp-cl
