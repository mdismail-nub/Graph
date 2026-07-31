# Undirected Graph Representation (C++)

This repository demonstrates two common ways to represent an **undirected graph** in C++.

## Input Format

```text
n m
u1 v1
u2 v2
...
um vm
```

- `n` → Number of nodes (vertices)
- `m` → Number of edges
- `u` and `v` → Two connected nodes

Since the graph is **undirected**, an edge connects both nodes. If `u` is connected to `v`, then `v` is also connected to `u`.

---

## 1. Adjacency List

```cpp
vector<int> adj[n + 1];
```

For every edge:

```cpp
adj[u].push_back(v);
adj[v].push_back(u);
```

Each node stores a list of all its neighboring nodes.

**Time Complexity:** `O(m)`  
**Space Complexity:** `O(n + m)`

---

## 2. Adjacency Matrix

```cpp
int adj[n + 1][n + 1];
```

For every edge:

```cpp
adj[u][v] = 1;
adj[v][u] = 1;
```

- `1` → An edge exists between `u` and `v`
- `0` → No edge (initialize the matrix with `0` before use)

**Time Complexity:** `O(m)`  
**Space Complexity:** `O(n²)`

---

## Which One Should You Use?

- ✅ **Adjacency List:** Best for sparse graphs and most graph algorithms.
- ✅ **Adjacency Matrix:** Best when fast edge lookup (`O(1)`) is required or the graph is dense.
