# Graph Representation in C++

This folder contains beginner-friendly implementations of different **graph representation techniques** in C++.

## Folder Structure

```
Representation of Graphs/
│
├── Directed/
│   ├── Adjacency List
│   ├── Adjacency Matrix
│   ├── Weighted Adjacency List
│   └── Weighted Adjacency Matrix
│
└── Undirected/
    ├── Adjacency List
    ├── Adjacency Matrix
    ├── Weighted Adjacency List
    └── Weighted Adjacency Matrix
```

## Topics Covered

- Directed Graph
- Undirected Graph
- Weighted Directed Graph
- Weighted Undirected Graph
- Adjacency List Representation
- Adjacency Matrix Representation

## Prerequisites

Before learning these implementations, you should know:
- Arrays
- Vectors (`std::vector`)
- Pairs (`std::pair`)
- Basic C++ Syntax

## Which Representation Should You Use?

| Representation | Space Complexity | Best For |
|---------------|------------------|----------|
| Adjacency List | `O(n + m)` | Sparse graphs |
| Adjacency Matrix | `O(n²)` | Dense graphs & fast edge lookup |

Where:
- `n` = Number of nodes (vertices)
- `m` = Number of edges

## Target Audience

These implementations are written for **beginners** who are starting Graph Theory and preparing for **Data Structures & Algorithms (DSA)** or **Competitive Programming**.

Happy Coding! 🚀
