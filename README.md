# Routing problem

Check out [results_visualized](results_visualized.md) for plots of optimal solutions.

## Mathematical formulation

Variables/parameters:

 - $N_w$ : number of warehouses
 - $N_d$ : number of demand points
 - **$x_{ij}$ : $1$ if demand point $j$ is supplied by warehouse $i$**
 - $c_{ij}$ : cost of supplying demand point $j$ from warehouse $i$ 
 - **$o_{i}$ : $1$ if warehouse $i$ is used**
 - $l_i$ : minimum required deliveries to open warehouse $i$ 
 - $u_i$ : maximum capacity of warehouse $i$
 - $d_i$ : demand at demand point $j$


Minimize the objective cost function
$$\sum_{i=0}^{N_w -1} \sum_{j=0}^{N_d -1} c_{ij} x_{ij},$$

such that

$$l_i*o_i \leq \sum_{j = 0}^{N_{d-1}} x_{ij} d_j \leq u_i*o_i \forall i$$

$$\sum_{i = 0}^{N_w-1} x_{ij} = 1 \forall j$$

$$x_{i,j} = \{0,1\} \forall i,j$$

$$o_i = \{0,1\} \forall i$$
