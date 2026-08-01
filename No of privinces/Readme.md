# Number of Provinces (DFS)

This program solves the **Number of Provinces** problem using **Depth First Search (DFS)**.

The given graph is represented as an **adjacency matrix**. The program first converts it into an **adjacency list** and then uses DFS to count the number of connected components (provinces).

---

## Input Format

```text
n
adjacency_matrix
```

- `n` → Number of cities (vertices)
- `adjacency_matrix[i][j]`
  - `1` → City `i` is directly connected to city `j`
  - `0` → No direct connection

---

## Example

**Input**

```text
3
1 1 0
1 1 0
0 0 1
```

**Output**

```text
2
```

**Explanation**

- Province 1: `{0, 1}`
- Province 2: `{2}`

Hence, the answer is **2**.

---

## Algorithm

1. Read the adjacency matrix.
2. Convert the matrix into an adjacency list.
3. Traverse each unvisited node using DFS.
4. Every time a new DFS starts, increment the province count.
5. Return the total number of provinces.

---

## Complexity

- **Time Complexity:** `O(V²)`
- **Space Complexity:** `O(V + E)`

Where:
- `V` = Number of vertices (cities)
- `E` = Number of edges

---

## Note

- A **province** is a group of directly or indirectly connected cities.
- The graph is **undirected**, so every connection is considered in both directions.
- DFS is used to find all connected components.

---

## 📖 Resources

- **Video Explanation (Striver):** https://youtu.be/ACzkVtewUYA?si=FtzKSe8tO6nuZjAm
- **Practice Problem (LeetCode):** https://leetcode.com/problems/number-of-provinces/
