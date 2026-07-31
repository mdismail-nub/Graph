# Directed Graph Representation (C++)

This repository demonstrates two common ways to represent a **directed graph** in C++.

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
- `u` → Source node
- `v` → Destination node

Since the graph is **directed**, an edge exists only from **`u` → `v`**. The reverse edge (`v` → `u`) is **not** added.

---

## 1. Adjacency List

```cpp
vector<int> adj[n + 1];
```

For every edge:

```cpp
adj[u].push_back(v);
```

This stores all nodes that can be reached directly from `u`.

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
```

- `1` → Edge exists from `u` to `v`
- `0` → No edge (initialize the matrix with `0` before use)

**Time Complexity:** `O(m)`  
**Space Complexity:** `O(n²)`

---

## Which One Should You Use?

- ✅ **Adjacency List:** Preferred for most graph algorithms and sparse graphs.
- ✅ **Adjacency Matrix:** Useful for fast edge lookup (`O(1)`) or dense graphs.
