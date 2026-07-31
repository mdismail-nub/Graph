# Weighted Directed Graph Representation (C++)

This repository demonstrates two common ways to represent a **weighted directed graph** in C++.

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
- `u` → Starting node
- `v` → Destination node
- `w` → Weight (cost) of the edge

Since the graph is **directed**, an edge goes **only from `u` to `v`**. We do **not** add the reverse edge.

---

## 1. Adjacency List

```cpp
vector<pair<int, int>> adj[n + 1];
```

Each node stores a list of its outgoing edges.

For an edge `(u, v)` with weight `w`:

```cpp
adj[u].push_back({v, w});
```

Here:
- `first` = Destination node (`v`)
- `second` = Edge weight (`w`)

**Time Complexity:** `O(m)`  
**Space Complexity:** `O(n + m)`

---

## 2. Adjacency Matrix

```cpp
int adj[n + 1][n + 1];
```

Each cell `adj[u][v]` stores the weight of the edge from `u` to `v`.

```cpp
adj[u][v] = weight;
```

If there is no edge, the value should typically be initialized to `0` or `INF` depending on the problem.

**Time Complexity:** `O(m)`  
**Space Complexity:** `O(n²)`

---

## Which One Should You Use?

- ✅ **Adjacency List:** Best for sparse graphs and most graph algorithms (BFS, DFS, Dijkstra, etc.).
- ✅ **Adjacency Matrix:** Useful when you need constant-time edge lookup or the graph is dense.
