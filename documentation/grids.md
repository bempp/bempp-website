---
title: Creating grids
---

This tutorial demonstrates basic features of dealing with grids in Bempp.
Simple grids can be easily created using built-in commands.
More complicated grids can be imported in the [Gmsh](http://gmsh.info/) format.

## Creation of basic grid objects
Let us create our first grid, a simple regular sphere.

```python
import bempp.api
import numpy as np
grid = bempp.api.shapes.regular_sphere(3)
```

The function `regular_sphere` creates a sphere by refining a base octahedron.
The number of elements in the sphere is $8\times4^n$, where $n$ is the refinement level.
