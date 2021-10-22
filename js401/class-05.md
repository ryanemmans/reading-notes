# CLASS 5 NOTES - Implementation: Linked Lists

## ***Big O: Analysis of Algorithm Efficiency***

[https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)

- - -

### **Big O notation** - used to describe efficiency of an algorithm or function.

- Evaluated based on 2 factors:
  1. Running Time - ***'Time'*** efficiency / complexity
      - The amount of time a function needs to complete.
  2. Memory Space - ***'Space'*** efficiency / complexity
      - The amount of memory resources a function uses to store data and instructions.

Big O describes *Worst Case* of efficiency of an algorithm.

- 4 Key Areas for analysis:
  1. Input Size
  2. Units of Measurement
  3. Orders of Growth
  4. Best Case, Worst Case, and Average Case

### **Input Size** - size of the parameter values that are read by the algorithm.

### **Units of Measurement** - evaluate a function for **Time** and **Space** complexity.

- To quanitify *Running Time* in our analysis...
  - Time in milliseconds
  - Number of operations - # of lines of code
  - Number of "Basic Operations" - contribute most to running time. (usually innermost loop)

- To quanitify *Memory Space* ...
  - Space needed to hold code
  - Space needed to hold input data
  - Space needed to hold output data
  - Space needed to hold working space during calculation

Working Space - creation of variables and reference points as function performs calculations.

- Includes Stack Space

### **Orders of Growth** - Overall efficiency

- Use input size *`n`* and measure overall Units of Space and Time required for given input size *`n`*. As the value of *`n`* grows, Order of Growth represents increase in Running Time or Memory Space.

**Constant Complexity** - always uses the same amount of time or space regardless of inputs.

**Logarithmic Complexity** - as rate of complexity growth decreases, the greater our value of *`n`*.

**Linear Complexity** - size of inputs *`n`* will directly determine amount of Memory Space used and Running Time length.

**Linearithmic Complexity** - describes a growth rate of *`n`* by *`lgn`*.

**Quadratic Complexity** - describes an algorithm with complexity growing at a rate of input size *`n`* multiplied by *`n`*.

**Cubic Complexity** - higher degree of what makes the quadratic complexity grow at such a high rate.

**Exponential Complexity** very rapidly growing complexity, whatever input size *`n`*, we are performing the same number of iterative or recursive loops as *`n`*.

**Factorial Complexity** - Space and Time requirements grow extremely fast, relative to input size.

### **Worst Case, Best Case, Average Case**

**Worst Case** - The efficiency for the worst possible input of size *`n`*

- Runs the longest for all possible inputs of *`n`*

**Best Case** - The efficiency for the best possible input of size *`n`*

- Runs the quickest for all possible inputs of *`n`*

**Average Case** - The efficiency for a “typical” or “random” input of size *`n`*

- Makes typical assumption about possible inputs of size *`n`* and how they might affect efficiency.

- - -

## ***Linked Lists***

[https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

- - -

### **Linked List** - A sequence of Nodes that are connected or linked to each other. Each Node references the next Node in the link.

Two types of Linked List - ***Singly*** and ***Doubly***.

**Singly** - Number of references the node has.

- Only one reference which to the Next node in a linked list.

**Doubly** - Two (double) references within the node.

- Reference to both the Next and Previous node.

**Node** - Individual items/links that live in a linked list.

- Each node contains the data for each link.

**Next** - Each node contains a property called Next, which contains the reference to the next node.

**Head** - Reference of type Node to the first node in a linked list.

**Current** - Reference of type Node to the node that is currently being looked at.

- New Current variable is created at Head to guarantee you are starting from the beginning of the linked list.

- - -

## ***What’s a Linked List, Anyway? [Part 1]***

[https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

- - -

### **Linear data structures** - Sequence and order to how linked lists are constructed and traversed.

### **Memory management**

### **Parts of a linked list**

- Nodes (or elements)
  - Head - Starting point is reference to first Node
  - End of list points to an empty value, or `null`

Singly Linked List - only go in one direction.

Doubly Linked List - two references contained within each node: a reference to the next node, as well as the previous node.

Circular Linked List - has a node that acts as tail of the list, and the node after the tail is the beginning of the list.

- - -

## ***What’s a Linked List, Anyway? [Part 2]***

[https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

- - -

### **Big O Notation**

- A way of evaluating the performance of an algorithm.

### **Growing a Linked List**

- We can add elements and remove elements from a linked list, similarly to an array.

- - -

[back](../README.md)
