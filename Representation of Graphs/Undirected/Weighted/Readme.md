# Weighted Undirected Graph Representation (C++)

This repository demonstrates two common ways to represent a **weighted undirected graph** in C++.

## Input Format

```text
n m
u1 v1 w1
u2 v2 w2
...
um vm wm
```

- `n` → Number of nodes (vertices)
- `m` → Number of edges
- `u` and `v` → Two connected nodes
- `w` → Weight (cost) of the edge

Since the graph is **undirected**, an edge connects both nodes. Therefore, the edge is stored in both directions.

---

## 1. Adjacency Matrix

```cpp
int adj[n + 1][n + 1];
```

For every edge:

```cpp
adj[u][v] = weight;
adj[v][u] = weight;
```

Each cell stores the weight of the edge between two nodes.

> If there is no edge, initialize the matrix with `0` or `INF` depending on the problem.

**Time Complexity:** `O(m)`  
**Space Complexity:** `O(n²)`

---

## 2. Adjacency List

```cpp
vector<pair<int, int>> adj[n + 1];
```

For every edge:

```cpp
adj[u].push_back({v, weight});
adj[v].push_back({u, weight});
```

Each pair stores:
- `first` → Neighbor node
- `second` → Edge weight

**Time Complexity:** `O(m)`  
**Space Complexity:** `O(n + m)`

---

## Which One Should You Use?

- ✅ **Adjacency List:** Best for sparse graphs and algorithms like Dijkstra, Prim's, DFS, and BFS.
- ✅ **Adjacency Matrix:** Best for dense graphs or when fast edge lookup (`O(1)`) is required.
