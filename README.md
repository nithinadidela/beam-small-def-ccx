# Small deflection of a cantilever beam simulation with CalculiX 2.15
​
This is a part of our undergraduate project titled 'Aeroelastic modelling of insect flight' carried out in the school of Mechanical sciences, Indian Institute of Technology Goa.

* Authors: Nithin Adidela, Revanth Sharma, Y. Sudhakar

* email: {nithin.adiela.16003,revanth.sharma.16003,sudhakar}@iitgoa.ac.in

The  simulation is tested with CalculiX 2.15 in a machine running Ubuntu 18.04.

## Highlights 

* l = 8 m
* h = 1 m
* t = 1 m

* Number of elements 8*2*2

* E = 210 GPa
* ν = 0.3
* Fy = 9 MN


## Domain Description

The dimensions of the cantilever beam are length, l is 8 m. Height, h is 1 m. Thickness t is 1 m. Mesh element type is he20r which is a   3-D quadratic beam element. Elasticity Modulus of the material used is 210 GPa; Poisson’s ratio is 0.3; 

## Boundary Conditions

Degrees of freedom of the fixed end nodes are arrested along X, Y, and Z  and the degree of freedom of all the nodes is arrested along the Z axis. 

Concentrated Load of 10 N is applied after equally dividing it among the free-end nodes along the negative Y-axis. The domain is shown in the figure

## Running the case
​
### Pre-processing 

> $ cgx -b beam.fbd

### Running

> $ ccx beam | tee beam.log

### Post-processing 

> $ cgx -v beam.frd

## Outputs

To visualize the x-directional displacement,

> $ ds 1 e 1

To visualize the y-directional displacement,

> $ ds 1 e 2

To visualize the z-directional displacement,

> $ ds 1 e 3

To visualize the σxx,

> $ ds 2 e 1

To visualize the σyy,

> $ ds 2 e 2

To visualize the σzz,

> $ ds 2 e 3

To visualize the von-Mises stress,

> $ ds 2 e 7



