# Cut Set

Set of edges that disconnects the graph
cut set of size 1 ->  bridge

**Capacity** of cut set is sum of edge weights of a cut set

**Fundamental Cut set** with respect to a tree T has only one branch edge, the rest are chord edges. 

#### Ring sum ($\Delta$) 
- Ring sum of two graphs is a graph which has vertices from both graphs, bu only the edges that are there in either, but no in both.
Eg. $\{d,e,f\}\ \Delta\ \{f,g,h\} = \{d,e,g,h\}$

*Ring sum of two cut sets will lead to a new cut set or a disjoint union of two cut sets*

#### Separating Vertex Set
- Set of vertices whose removal disconnects the graph.
- **Cut vertex** is when a single vertex's removal can disconnect the graph.


#### Whitney's Inequality
Let $\lambda(G)$ be the number of edges in the smallest cut set,
let K(G) be the number of vertices in the smallest separating vertex set.
and let the min degree be $\delta(G)$ 
$$K(G) \leq \lambda(g) \leq \delta(G)$$
[Planar Graphs](planar-graphs.md)