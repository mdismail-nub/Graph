# Breadth First Search (BFS) in C++

This program implements **Breadth First Search (BFS)** on an **undirected graph** using an **adjacency list**.

BFS starts from **node 1** and visits all reachable nodes level by level using a **queue**.

---

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

---

## Example

**Input**

```text
5 5
1 2
1 3
2 4
3 5
4 5
```

**Output**

```text
1 2 3 4 5
```

---

## How It Works

1. Start BFS from node `1`.
2. Mark it as visited and push it into the queue.
3. While the queue is not empty:
   - Remove the front node.
   - Visit it.
   - Push all its unvisited neighbors into the queue.
4. Continue until the queue becomes empty.

---

## Complexity

- **Time Complexity:** `O(V + E)`
- **Space Complexity:** `O(V)`

Where:
- `V` = Number of vertices
- `E` = Number of edges

---

## Note

- This implementation assumes the graph is **connected**.
- If the graph is **disconnected**, BFS starting from node `1` will visit only the nodes reachable from `1`. To traverse the entire graph, run BFS from every unvisited node.
