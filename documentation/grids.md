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

Another way to create a sphere is by specifying the width of the elements.
The following code will create an unstructured spherical grid with a grid size of roughly 0.1.
```python
grid = bempp.api.shapes.sphere(h=0.1)
```

The ```shapes``` module contains functions for a number of shapes, including spheres, ellipsoids, cubes, screens, and the Nasa almond shape.

## Creating grids from connectivity data
If the shape you require is not provided, a grid may be created using connectivity data: arrays containing the nodes (or vertices) and the element definitions.

The vertices may be defined as follows.
```python
import numpy as np
vertices = np.array([[0, 1, 1, 0],
                     [0, 0, 1, 1],
                     [0, 0, 0, 0]])
```
The array `vertices` contains the $(x,y,z)$ coordinates of the four vertices of the unit square in the $x$-$y$ plane. Note that each column is the coordinate of one point.

We now define two elements by specifying how the vertices are connected.
```python
elements = np.array([[0, 1],
                     [1, 2],
                     [3, 3]])
```
The first element connects the vertices 0, 1 and 3.
The second element connects the vertices 1, 2 and 3.
Similarly to the vertices array, each column is an element.

To create a grid from these two elements we simply run the following command.
Bempp assumes that each element is defined such that the normal direction obtained with the right-hand rule is outward pointing.
Elements with inward pointing normals will cause errors in computations.
Normal directions can be visually checked for example by loading a mesh in Gmsh and displaying the normals.

```python
grid = bempp.api.grid.Grid(vertices, elements)
```

## Iterating through grids
For many Bempp usage scenarios, the internals of the grid object are not important.
However, sometimes it may be useful to iterate through a grid and retrieve information from individual elements.
Internally, entities in Bempp are stored by codimension.
For surface meshes, this translates as follows:

+ Codim-0 entities: Elements (triangles) of the mesh
+ Codim-1 entities: Edges of the mesh
+ Codim-2 entities: Vertices of the mesh

For example, the following snippet can be used to show the number of elements in the first sphere mesh above.

```python
# Create the grid
import bempp.api
grid = bempp.api.shapes.regular_sphere(3)

# Print the number of elements
number_of_elements = grid.entity_count(0)
print("The grid has {0} elements.".format(number_of_elements))
```

In order to obtain all vertices and elements of a mesh, the following commands can be used.

```python
vertices = grid.vertices
elements = grid.elements
```

If the grid was created using connectivity data, then `vertices` and `elements` will be exactly the input data.

We can also iterate through entities and obtain geometric information about them.
Iterators may be directly used in for loops.

```python
for element in grid.entity_iterator(0):
    pass
```

We now print the area of every element in the mesh.

```python
for i, element in enumerate(grid.entity_iterator(0)):
    print("Area of element {0}: {1}".format(i, element.geometry.volume))
```
