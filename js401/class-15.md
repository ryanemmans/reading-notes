# CLASS 15 NOTES - Trees

[https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

- - -

## **Common Terminology**

- **Node** - (tree) a component which may contain it’s own values, and references to other nodes
- **Root** - node at the beginning of the tree
- **K** - number that specifies maximum number of children any node may have in a k-ary tree.
  - In a binary tree, `k = 2`.
- **Left** - reference to one child node, in a binary tree
- **Right** - reference to the other child node, in a binary tree
- **Edge** - link between a parent and child node
- **Leaf** - node that does not have any children
- **Height** - number of edges from the root to the furthest leaf

![Sample Tree](./img/sample-tree.png)

## Traversals

Allows us to search for a node, print out contents of a tree, and more

- Two categories - Depth first, Breadth first

### Depth First

Traversal of going through the *height* of the tree first

- Utilizes a stack (FILO) and recursion
  - Pre-order: root >> left >> right
  - In-order: left >> root> right
  - Post-order: left >> right >> root

### Breadth First

Iterates through a tree by going through each level node-by-node.

- Utilizes a queue (FIFO)

## Binary Trees Vs K-ary Trees

- Binary trees restrict the number of children to two
  - No specific sorting order for a binary tree.
  - Nodes can be added into a binary tree wherever space allows.

## K-ary Trees

- When nodes are able have more than 2 child nodes.
  - `K` refers to max number of children each Node can have.
  - Breadth first traversal (Queue)
    - Moves down a list of children of length `k` instead of checking for left and right

## Binary Search Trees (BST)

- All values *smaller* than the `root` are placed to the left
- All values *larger* that the `root` are placed to the right

- - -

[back](../README.md)
