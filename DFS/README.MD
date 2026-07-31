# Depth First Search (DFS) in C++

This program implements **Depth First Search (DFS)** on an **undirected graph** using an **adjacency list** and **recursion**.

DFS starts from **node 0** and explores as deep as possible before backtracking.

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
5 4
0 1
0 2
1 3
2 4
```

**Output**

```text
0 1 3 2 4
```

> **Note:** DFS traversal may vary depending on the order of the adjacency list.

---

## Algorithm

1. Start DFS from node `0`.
2. Mark the current node as visited.
3. Visit the current node.
4. Recursively visit all unvisited adjacent nodes.
5. Backtrack when no unvisited neighbor remains.

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
- For a **disconnected graph**, run DFS from every unvisited node to traverse all connected components.

---

## 📖 Resources

- **Video resource: https://youtu.be/Qzf1a--rhp8?si=quYDNN4fB1XfsguJ
- **Practice Problem (GeeksforGeeks):** https://www.geeksforgeeks.org/problems/depth-first-traversal-for-a-graph/1
