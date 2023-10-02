# Shortest Path

## Single Source Shortest Path
### Dijkstra's Algorithm
- Greedy Method
- Needs non-negative edge weights.
#### Algorithm
- Initialize SPT Set, and distance array.
- Assign INF to all vertices in distance and source vertex as 0.
- Pick a vertex not in SPTS, but is the least edge to an edge in SPTS.
- Update the distance values of all adjacent vertices to u.
- For an adjacent vertex v, the distance is updated if the **direct path**(source-v + v-u) is lesser than the **current best path**(value in distance array). 


### Bellman Ford
- Dynamic Programming Solution 
- Can have -ve egde weight
- no negative cycle
#### Algorithm
- Initialize distance array with all values INF and source vertex as 0.
- for each edge u-v update dist[v] if dist[u] + egde(u,v) < edge[v]
- repeat this until no changes are made. (v-1 is max).

## All Source Shortest Path

### Johnson's Algorithm




[Network Flow](network-flow)