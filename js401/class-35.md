# CLASS 35 NOTES - Graphs

- [https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)

- - -

A **graph** is a non-linear data structure

- A collection of `vertices` (or `nodes`) potentially connected by line segments named `edges`.

## Terminology

- **Vertex** - aka Node, data object that can have zero or more adjacent vertices
  - Ex: {a,b,c,d,e,f}
- **Edge** - connection between two nodes
  - Ex: {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}
- **Neighbor** - adjacent node, connected via an edge
- **Degree** - number of edges connected to a vertex

## Directed vs Undirected

- **Undirected Graph** - each edge is undirected or bi-directional
  - Does not move in any direction
- **Directed Graph (Digraph)** - every edge is directed
  - Each node is directed at another node
    - Specific requirement of which node should be referenced next

## Complete vs Connected vs Disconnected

- **Complete Graph** - *all* vertices / nodes are connected to *all* other nodes
- *Connected Graph* - *all* vertices / nodes have *at least one* edge
  - A Tree is a form of a connected graph
- *Disconnected Graph* - some vertices / nodes may not have edges
  - Possible for standalone nodes (aka islands)

## Acyclic vs Cyclic

- **Cycle** - a path of a positive length that starts and ends at the same vertex
- **Acyclic Graph** - *directed* graph *without* cycles
  - Also called a **DAG**, or represented as a **tree**
- **Cyclic Graph** - has cycles

## Graph Representation

### Adjacency Matrix

- Represented through a 2-D array.
  - If *n* vertices, then *n x n* Boolean matrix
- Each row / column represents each vertex
  - 1 if there *is* a connection / edge, 0 if there is *no* connection / edge

```js
    a  b  c  d  e  f
[    
a [ 0, 0, 1, 1, 0, 0 ],
b [ 0, 0, 1, 0, 0, 1 ],
c [ 1, 1, 0, 0, 1, 0 ],
d [ 1, 0, 0, 0, 1, 0 ],
e [ 0, 0, 1, 1, 0, 1 ],
f [ 0, 1, 0, 0, 1, 0 ]
];
```

- **Sparse** - graph with very few connections
- **Dense** - graph with many connections

### Adjacency List

- Most common way to represent graphs
  - Collection of linked lists or array that lists all other connected vertices
  - Easy to view connections of vertices

```js
{a} -> c -> d
{b} -> c -> f
{c} -> a -> b -> e
{d} -> a -> e
{e} -> c -> d -> f
{f} -> b -> e
```

## Weighted Graphs

A graph with numbers (called "weights") assigned to its edges

Weight matrix example:

```js
    a  b  c  d
[    
a [ 0, 4, 3, 9 ],
b [ 4, 0, 0, 5 ],
c [ 3, 0, 0, 6 ],
d [ 9, 5, 6, 0 ],
];
```

Adjacency lists must include *both* weight *and* name of adjacent vertex:

```js
{a} -> b,4 -> d,9 -> c,3
{b} -> a,4 -> d,5
{c} -> a,3 -> d,6
{d} -> a,9 -> b,5 -> c,6
```

`{vertex, weight}` connection can be represented through a key/value pair data structure.

## Traversals

### Breadth First

- Start at specific vertex
- Similar to a tree, except graphs have cycles.

### Depth First

## Real World Uses of Graphs

- - -

[back](../README.md)
