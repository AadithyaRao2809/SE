# Graph Coloring

Coloring a graph - assigning color to vertices such that no two adjacent vertices don't have same color.

**Chromatic number** minimum number of colors needed to color a graph

**Matching** Set of edges without common vertices

##### Common graphs Chromatic number
- Kn - n
- bipartite 2
- odd cycle - 3
- even cycle - 2
- tree - 2


#### Greedy Algorithm for Graph Coloring
Color the currently chosen vertex with the lowest color that is not used by the adjacent vertices.

This algorithm always gives a valid color, but it may not be the least number of colors. It is also dependent on the order that the vertices are chosen in.

#### Welsh Powell Algorithm for Graph Coloring
1. Find the degree of each vertex
2. List the vertices in order of decreasing degrees.
3. Color the first vertex with a color. 
4. Go to all the vertices not connected to the colored vertex and color them the same color.
5. Continue this process until all the vertices are colored.

**Chromatic Partition** is the number of vertices in the largest  independent set. An independent set is a set of vertices where not two vertices in the set  are adjacent to each other. 

[Chromatic Polynomial](chromatic-polynomial)