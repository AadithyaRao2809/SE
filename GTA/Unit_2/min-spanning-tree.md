# Minimum Spanning Tree

### Kruskal's Algorithm
- Start with empty graph and sort edges in ascending order
- Pick smallest edge
- check if adding that edge forms a cycle
- If no cycle add it
- Repeat until v-1 edges are added.

### Reverse Delete Algorithm
- Start with full graph, sort edges in Descending order
- Pick largest edge
- If it is not a bridge, discard the edge.
- Repeat until v-1 edges are remaining.


### Boruvka's algorithm
- Start with n one-node trees
- find the shortest edge in a component that connects to an edge in another component.
-  Add that edge to the tree.
- Repeat until the number of components is 1.

### Prim's Algorithm
- Initialize an empty MST Set.
- start with some random vertex u and add it to MST set.
- Pick the vertex neighboring to any vertex in MST Set with minimum edge weight, which does not form a cycle
- Repeat until MST Set has v Vertices.

[Shortest Path](shotrest-path)