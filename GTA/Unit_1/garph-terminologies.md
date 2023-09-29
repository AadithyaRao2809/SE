# Graph Terminologies

- **Order** no. of vertices
- **Size** no. of edges
- **Simple graph** no loops, no parallel edges
- **Degree of vertex** no of edges incident on vertex
- **Pendant** vertex with degree 1
- **Min degree** $\delta(G)$ - least degree vertex
- **Max degree** $\Delta(G)$ - largest degree vertex
- **Chromatic Number** Minimum number of colors to color all vertices such that no two adjacent vertices have same color.
- **Subgraph** G is subgraph of H if $V(G)\subseteq V(H)$ and $E(G)\subseteq E(H)$ 
- 
### Types of Graphs
- **Complete graph** $K_n$ - on edge b/w each pair of vertices.
- **Cycle** $C_n$ - path that starts and ends on same vertex without repeating.
- **Bipartite** two sets $V_1$ and $V_2$ that dont have common edges.
- **Complete Bipartite** $K_{m,n}$ - Bipartite graph where every vertex in $V_1$ is connected to every vertex in $V_2$ .
- **Connected Graph** path b/w every pair of vertices is connected
- **Isomorphic Graph** G is isomorphic to H if they have same number of vertices and edges, and edge connectivity is retained.
- **Regular Graph** all vertices having same degree


### Properties
- **Distance** shortest path b/w vertices
- **Eccentricity** Max dist. from a vertex to all other vertex.
- **Radius** Min eccentricity
- **Diameter** Max eccentricity
- **Central Point** vertex whose eccentricity matches the radius.
- **Center** set of all central points.
- **Girth** length of Shortest cycle
- **Circumference** length of largest cycle
- Sum of degree of vertices = twice the number of edges $\sum\limits_{i=1}^{n}d(v_i)=2e$
- Number of vertices with odd degree are always even.


[Eulerian Graph](eulerian-graph.md)