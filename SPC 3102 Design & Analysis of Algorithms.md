### DESIGN AND ANALYSIS OF ALGORITHMS - Lecture 1 Summary

---

### **Algorithm Definition**

* **Algorithm** : A finite sequence of instructions, each clear and executable in a finite time and effort.

### **Algorithm Criteria**

* **Input** : Zero or more externally supplied quantities.
* **Output** : At least one quantity produced.
* **Definiteness** : Instructions must be clear and unambiguous.
* **Finiteness** : The algorithm must terminate after a finite number of steps.
* **Effectiveness** : Instructions must be simple enough to carry out.

### **Algorithm Specification**

1. **Natural Language** : Written in plain language, e.g., English (requires clarity).
2. **Flowchart** : Graphical representation, useful for small/simple algorithms.
3. **Pseudo-code** : Combination of programming constructs and informal language.

### **Pseudo-code Conventions**

1. **Comments** : Begin with `//` and continue to the end of the line.
2. **Blocks** : Indicated with braces `{` and `}`.
3. **Identifiers** : Begin with a letter (data types not explicitly declared).
4. **Compound Data Types** : Example `Node` structure with fields like `data` and pointers.
5. **Assignment** : `<Variable> := <expression>`.
6. **Boolean Values** : `TRUE` and `FALSE` used with logical operators like AND, OR, NOT.
7. **Loops** :

* **While Loop** : `While <condition> do { <statements> }`.
* **For Loop** : `For variable := value1 to value2 step step do { <statements> }`.
* **Repeat-Until** : `repeat { <statements> } until <condition>`.

1. **Conditional Statements** :

* Simple: `If <condition> then <statement>`.
* With Else: `If <condition> then <statement1> Else <statement2>`.
* **Case Statement** : `Case { : <condition1>: <statement1> ... : else: <statement> }`.

1. **Input/Output** : `read` and `write` for input and output operations.
2. **Procedure** : `Algorithm <Name> (<Parameters>)`.

Here are some examples of pseudo-code programs demonstrating various concepts such as loops, conditionals, and functions:

##### **Example 1: Finding the Maximum of Two Numbers**

This example demonstrates a simple comparison to find the maximum of two numbers.

```plaintext
Algorithm MaxOfTwoNumbers(A, B)
    // A and B are two numbers
    If A > B then
        Return A
    Else
        Return B
```

##### **Example 2: Sum of First N Natural Numbers**

This example shows how to calculate the sum of the first `n` natural numbers using a loop.

```plaintext
Algorithm SumOfFirstNNumbers(n)
    // n is the number of natural numbers
    sum := 0
    For i := 1 to n do
        sum := sum + i
    EndFor
    Return sum
```

##### **Example 3: Factorial of a Number**

This program calculates the factorial of a given number `n` using a for loop.

```plaintext
Algorithm Factorial(n)
    // n is the number for which we need the factorial
    result := 1
    For i := 1 to n do
        result := result * i
    EndFor
    Return result
```

##### **Example 4: Fibonacci Sequence**

This program generates the first `n` terms of the Fibonacci sequence.

```plaintext
Algorithm Fibonacci(n)
    // n is the number of terms to generate
    a := 0
    b := 1
    Print a
    Print b
    For i := 3 to n do
        c := a + b
        Print c
        a := b
        b := c
    EndFor
```

##### **Example 5: Linear Search**

This example performs a linear search to find the index of an element in an array.

```plaintext
Algorithm LinearSearch(A, target)
    // A is the array and target is the element to search for
    For i := 1 to length of A do
        If A[i] == target then
            Return i
        EndIf
    EndFor
    Return -1 // Element not found
```

##### **Example 6: Bubble Sort**

This example demonstrates the Bubble Sort algorithm to sort an array in ascending order.

```plaintext
Algorithm BubbleSort(A)
    // A is the array to sort
    n := length of A
    For i := 1 to n-1 do
        For j := 1 to n-i do
            If A[j] > A[j+1] then
                // Swap A[j] and A[j+1]
                temp := A[j]
                A[j] := A[j+1]
                A[j+1] := temp
            EndIf
        EndFor
    EndFor
EndAlgorithm
```

##### **Example 7: Finding Prime Numbers (Sieve of Eratosthenes)**

This is an example of the Sieve of Eratosthenes algorithm to find all prime numbers up to `n`.

```plaintext
Algorithm SieveOfEratosthenes(n)
    // n is the upper limit for finding prime numbers
    Create a boolean array isPrime of size n+1
    For i := 2 to n do
        isPrime[i] := true
    EndFor

    For p := 2 to sqrt(n) do
        If isPrime[p] == true then
            For i := p^2 to n step p do
                isPrime[i] := false
            EndFor
        EndIf
    EndFor

    // Print all primes
    For i := 2 to n do
        If isPrime[i] == true then
            Print i
        EndIf
    EndFor
EndAlgorithm
```

##### **Example 8: Finding the GCD of Two Numbers (Euclidean Algorithm)**

This program computes the greatest common divisor (GCD) of two numbers using the Euclidean algorithm.

```plaintext
Algorithm GCD(a, b)
    // a and b are the two numbers
    While b != 0 do
        temp := b
        b := a mod b
        a := temp
    EndWhile
    Return a
EndAlgorithm
```

##### **Example 9: Binary Search**

This example demonstrates how to perform a binary search on a sorted array.

```plaintext
Algorithm BinarySearch(A, target)
    // A is the sorted array and target is the element to find
    low := 1
    high := length of A
    While low <= high do
        mid := (low + high) / 2
        If A[mid] == target then
            Return mid
        Else If A[mid] < target then
            low := mid + 1
        Else
            high := mid - 1
        EndIf
    EndWhile
    Return -1 // Element not found
EndAlgorithm
```

These are basic examples that showcase different algorithm types such as searching, sorting, mathematical operations, and generating sequences. They provide a clear way to represent algorithms using pseudo-code without being tied to any particular programming language syntax.

### **Performance Analysis**

* **Objective** : Analyze the memory and time needed for a program to run.
* **Two Approaches** : Analytical methods (theoretical) and experimental methods (empirical).
* **Key Terms** :
* **Time Complexity** : The time required by an algorithm as a function of problem size.
* **Space Complexity** : The memory required by a program.

### **Time Complexity**

* **Definition** : The time an algorithm takes, expressed as a function of the input size `f(n)`.
* **Asymptotic Complexity** : Behavior of the algorithm's time as input size increases.
* **Factors Affecting Running Time** :
* Input characteristics.
* Compiler efficiency.
* Machine characteristics.

### **Measuring Running Time**

* **Factors** :

1. Input data size.
2. Quality of code and compiler optimizations.
3. Machine specifications.

### **Space Complexity**

* **Definition** : The amount of memory required by an algorithm.
* **Components** :
* **Instruction Space** : Space for compiled instructions.
* **Data Space** : Space for constants, variables, and dynamically allocated objects.
* **Environment Stack** : Space for function calls and partial executions.

### **Complexity of Algorithms**

* **Definition** : A function `f(n)` that defines the running time/space requirement of an algorithm in terms of input size.
* **Storage Complexity** : Typically a multiple of data size.
* **Types of Complexity** :
* **Best Case** : Minimum value of `f(n)`.
* **Average Case** : Expected value of `f(n)`.
* **Worst Case** : Maximum value of `f(n)`.

### **Asymptotic Notations**

* **Big-O (O)** : Upper bound, indicates worst-case growth rate.
* **Big-Omega (Ω)** : Lower bound, indicates best-case growth rate.
* **Big-Theta (Θ)** : Exact bound, indicates when the growth rate is the same.

### **Time Complexities**

* **Common Notations** :
* `O(1)`, `O(log n)`, `O(n)`, `O(n log n)`, `O(n^2)`, `O(n^3)`, `O(2^n)`, `O(n!)`.
* **Classes** :
* **Constant** : Time does not depend on the size of input.
* **Logarithmic** : Time increases slowly as input grows (e.g., binary search).
* **Linear** : Time increases linearly with input size.
* **n log n** : Common in divide-and-conquer algorithms.
* **Quadratic (n²)** : Time increases quadratically (e.g., bubble sort).
* **Cubic (n³)** : Time increases cubically.
* **Exponential (2^n)** : Time doubles with each increase in input.

### **Classification of Algorithms**

| **Complexity** | **Description**                                      | **Example**              |
| -------------------- | ---------------------------------------------------------- | ------------------------------ |
| Constant             | Executed once or a few times                               | Search in an unordered list    |
| Logarithmic          | Slow growth of execution time as `n`increases            | Binary search                  |
| Linear               | Time increases linearly with `n`                         | Linear search                  |
| n log n              | Occurs in divide-and-conquer algorithms                    | Merge sort, Quick sort         |
| Quadratic (n²)      | Slow for large problems; practical only for small problems | Bubble sort, Insertion sort    |
| Cubic (n³)          | Slow for larger problems                                   | Triple nested loops            |
| Exponential          | Time doubles with each increase in input size              | Certain brute-force algorithms |

### **Numerical Comparison of Different Algorithms**

* For a given problem size `n`, execution time can be analyzed for different algorithms.
* Algorithms like O(n²) or O(2^n) become impractical as input size grows due to excessive time complexity.

---

This summary encapsulates the key points from the lecture on  **Design and Analysis of Algorithms** . It outlines algorithm definition, criteria, pseudo-code conventions, performance analysis, and different complexities with examples.

# lecture 2 : Graphs

## What Are Graphs in Data Structure?

A graph is a non-linear kind of data structure made up of nodes or vertices and edges. The edges connect any two nodes in the graph, and the nodes are also known as vertices.

![what-is-graphs-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/what-is-graphs-in-data-structure.png)

This graph has a set of vertices V= { 1,2,3,4,5} and a set of edges E= { (1,2),(1,3),(2,3),(2,4),(2,5),(3,5),(4,50 }.

Now that you’ve learned about the definition of graphs in data structures, you will learn about their various types.

## Types of Graphs in Data Structures

There are different types of graphs in data structures, each of which is detailed below.

### 1. Finite Graph

The graph G=(V, E) is called a finite graph if the number of vertices and edges in the graph is limited in number

![FINITE-GRAPH-IN-GRAPHS-IN-DATA-STRUCTURE](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/FINITE-GRAPH-IN-GRAPHS-IN-DATA-STRUCTURE.png)

### 2. Infinite Graph

The graph G=(V, E) is called a finite graph if the number of vertices and edges in the graph is interminable.

![infinite-graph-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/infinite-graph-data-structure.png)

### 3. Trivial Graph

A graph G= (V, E) is trivial if it contains only a single vertex and no edges.

![trivial-graph-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/trivial-graph-data-structure.png)

### 4. Simple Graph

If each pair of nodes or vertices in a graph G=(V, E) has only one edge, it is a simple graph. As a result, there is just one edge linking two vertices, depicting one-to-one interactions between two elements.

![simple-graph-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/simple-graph-data-structure.png)

### 5. Multi Graph

If there are numerous edges between a pair of vertices in a graph G= (V, E), the graph is referred to as a multigraph. There are no self-loops in a Multigraph.

![multi-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/multi-graph-in-data-structure.png)

### 6. Null Graph

It's a reworked version of a trivial graph. If several vertices but no edges connect them, a graph G= (V, E) is a null graph.

![null-graph-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/null-graph-data-structure.png)

### 7. Complete Graph

If a graph G= (V, E) is also a simple graph, it is complete. Using the edges, with n number of vertices must be connected. It's also known as a full graph because each vertex's degree must be n-1.

![complete-graph-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/complete-graph-in-data-structure.png)

### 8. Pseudo Graph

If a graph G= (V, E) contains a self-loop besides other edges, it is a pseudograph.

![pseudo-graph-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/pseudo-graph-in-data-structure.png)

### 9. Regular Graph

If a graph G= (V, E) is a simple graph with the same degree at each vertex, it is a regular graph. As a result, every whole graph is a regular graph.

![regular-graph-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/regular-graph-in-data-structure.png)

### 10. Weighted Graph

A graph G= (V, E) is called a labeled or weighted graph because each edge has a value or weight representing the cost of traversing that edge.

![weighted-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/weighted-graph-in-data-structure.png)

### 11. Directed Graph

A directed graph also referred to as a digraph, is a set of nodes connected by edges, each with a direction.

![directed-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/directed-graph-in-data-structure.png)

### 12. Undirected Graph

An undirected graph comprises a set of nodes and links connecting them. The order of the two connected vertices is irrelevant and has no direction. You can form an undirected graph with a finite number of vertices and edges.

![undirected-graph-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/undirected-graph-in-data-structure.png)

### 13. Connected Graph

If there is a path between one vertex of a graph data structure and any other vertex, the graph is connected.

![connected-graph-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/connected-graph-in-data-structure.png)

### 14. Disconnected Graph

When there is no edge linking the vertices, you refer to the null graph as a disconnected graph.

![diconnected-graph-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/diconnected-graph-in-data-structure.png)

### 15. Cyclic Graph

If a graph contains at least one graph cycle, it is considered to be cyclic.

![cyclic-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/cyclic-graph-in-data-structure.png)

### 16. Acyclic Graph

When there are no cycles in a graph, it is called an acyclic graph.

![acyclic-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/acyclic-graph-in-data-structure.png)

### 17. Directed Acyclic Graph

It's also known as a directed acyclic graph (DAG), and it's a graph with directed edges but no cycle. It represents the edges using an ordered pair of vertices since it directs the vertices and stores some data.

![directed-acyclic-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/directed-acyclic-graph-in-data-structure.png)

### 18. Subgraph

The vertices and edges of a graph that are subsets of another graph are known as a subgraph.

![subgraph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/subgraph-in-data-structure.png)

After you learn about the many types of graphs in graphs in data structures, you will move on to graph terminologies.

## Terminologies of Graphs in Data Structures

Following are the basic terminologies of graphs in data structures:

* An edge is one of the two primary units used to form graphs. Each edge has two ends, which are vertices to which it is attached.
* If two vertices are endpoints of the same edge, they are adjacent.
* A vertex's outgoing edges are directed edges that point to the origin.
* A vertex's incoming edges are directed edges that point to the vertex's destination.
* The total number of edges occurring to a vertex in a graph is its degree.
* The out-degree of a vertex in a directed graph is the total number of outgoing edges, whereas the in-degree is the total number of incoming edges.
* A vertex with an in-degree of zero is referred to as a source vertex, while one with an out-degree of zero is known as sink vertex.
* An isolated vertex is a zero-degree vertex that is not an edge's endpoint.
* A path is a set of alternating vertices and edges, with each vertex connected by an edge.
* The path that starts and finishes at the same vertex is known as a cycle.
* A path with unique vertices is called a simple path.
* For each pair of vertices x, y, a graph is strongly connected if it contains a directed path from x to y and a directed path from y to x.
* A directed graph is weakly connected if all of its directed edges are replaced with undirected edges, resulting in a connected graph. A weakly linked graph's vertices have at least one out-degree or in-degree.
* A tree is a connected forest. The primary form of the tree is called a rooted tree, which is a free tree.
* A spanning subgraph that is also a tree is known as a [spanning tree.](https://www.simplilearn.com/tutorials/data-structure-tutorial/spanning-tree-in-data-structure "spanning tree.")
* A connected component is the unconnected graph's most connected subgraph.
* A bridge, which is an edge of removal, would sever the graph.
* Forest is a graph without a cycle.

Following that, you will look at the graph representation in this data structures tutorial.

## Representation of Graphs in Data Structures

Graphs in data structures are used to represent the relationships between objects. Every graph consists of a set of points known as vertices or nodes connected by lines known as edges. The vertices in a network represent entities.

The most frequent graph representations are the two that follow:

* Adjacency matrix
* Adjacency list

You’ll look at these two representations of graphs in data structures in more detail:

### Adjacency Matrix

* A sequential representation is an adjacency matrix.
* It's used to show which nodes are next to one another. I.e., is there any connection between nodes in a graph?
* You create an MXM matrix G for this representation. If an edge exists between vertex a and vertex b, the corresponding element of G, gi,j = 1, otherwise gi,j = 0.
* If there is a weighted graph, you can record the edge's weight instead of 1s and 0s.

#### Undirected Graph Representation

![graph-representation-in-data-structure-NEW.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/undirected-graph-representation-in-data-structure-NEW.png)

#### Directed Graph Representation

![directed-graph-representation-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/directed-graph-representation-in-data-structure.png)

#### Weighted Undirected Graph Representation

Weight or cost is indicated at the graph's edge, a weighted graph representing these values in the matrix.

![unweighted-graph-representation-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/unweighted-graph-representation-in-data-structure.png)

### Adjacency List

* A linked representation is an adjacency list.
* You keep a list of neighbors for each vertex in the graph in this representation. It means that each vertex in the graph has a list of its neighboring vertices.
* You have an arra[](https://www.simplilearn.com/tutorials/data-structure-tutorial/arrays-in-data-structure "array") of vertices indexed by the vertex number, and the corresponding [array](https://www.simplilearn.com/tutorials/data-structure-tutorial/arrays-in-data-structure "array") member for each vertex x points to a [singly linked list](https://www.simplilearn.com/tutorials/data-structure-tutorial/singly-linked-list "singly linked list") of x's neighbors.

#### Weighted Undirected Graph Representation Using Linked-List

![linked-list-adjancency-list-graph-represenatation-in-data-structure.](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/linked-list-adjancency-list-graph-represenatation-in-data-structure.png)

#### Weighted Undirected Graph Representation Using an Array

![arrayy-adjancency-list-graph-represenatation-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/arrayy-adjancency-list-graph-represenatation-in-data-structure.png)

You will now see which all operations are conducted in graphs data structure after understanding the representation of graphs in the data structure.

**Also Read: [Linked List in A Data Structure](https://www.simplilearn.com/tutorials/data-structure-tutorial/linked-list-in-data-structure "Linked List in A Data Structure")**

## Operations on Graphs in Data Structures

The operations you perform on the graphs in data structures are listed below:

* Creating graphs
* Insert vertex
* Delete vertex
* Insert edge
* Delete edge

You will go over each operation in detail one by one:

### Creating Graphs

There are two techniques to make a graph:

#### 1. Adjacency Matrix

The adjacency matrix of a simple labeled graph, also known as the connection matrix, is a matrix with rows and columns labeled by graph vertices and a 1 or 0 in position depending on whether they are adjacent or not.

#### 2. Adjacency List

A finite graph is represented by an adjacency list, which is a collection of unordered lists. Each unordered list describes the set of neighbors of a particular vertex in the graph within an adjacency list.

### Insert Vertex

When you add a vertex that after introducing one or more vertices or nodes, the graph's size grows by one, increasing the matrix's size by one at the row and column levels.

![add-vertex-operation-on-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/add-vertex-operation-on-graph-in-data-structure.png)

### Delete Vertex

* Deleting a vertex refers to removing a specific node or vertex from a graph that has been saved.
* If a removed node appears in the graph, the matrix returns that node. If a deleted node does not appear in the graph, the matrix returns the node not available.

![delete-vertex-operation-on-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/delete-vertex-operation-on-graph-in-data-structure.png)

### Insert Edge

Connecting two provided vertices can be used to add an edge to a graph.

![add-edge-operation-on-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/add-edge-operation-on-graph-in-data-structure.png)

### Delete Edge

The connection between the vertices or nodes can be removed to delete an edge.

![delete-edge-operation-on-graph-in-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/delete-edge-operation-on-graph-in-data-structure.png)

The types of graph traversal algorithms will be discussed next in the graphs in this data structures tutorial.

## Graph Traversal Algorithm

The process of visiting or updating each vertex in a graph is known as graph traversal. The sequence in which they visit the vertices is used to classify such traversals. Graph traversal is a subset of tree traversal.

There are two techniques to implement a graph traversal algorithm:

* Breadth-first search
* Depth-first search

### Breadth-First Search or BFS

[BFS](https://www.simplilearn.com/tutorials/data-structure-tutorial/bfs-algorithm "BFS") is a search technique for finding a node in a graph data structure that meets a set of criteria.

* It begins at the root of the graph and investigates all nodes at the current depth level before moving on to nodes at the next depth level.
* To maintain track of the child nodes that have been encountered but not yet inspected, more memory, generally you require a [queue.](https://www.simplilearn.com/tutorials/data-structure-tutorial/queue-in-data-structure "queue.")

Algorithm of breadth-first search

Step 1: Consider the graph you want to navigate.

Step 2: Select any vertex in your graph, say v1, from which you want to traverse the graph.

Step 3: Examine any two data structures for traversing the graph.

* Visited array (size of the graph)
* Queue data structure

Step 4: Starting from the vertex, you will add to the visited array, and afterward, you will v1's adjacent vertices to the queue data structure.

Step 5: Now, using the FIFO concept, you must remove the element from the queue, put it into the visited array, and then return to the queue to add the adjacent vertices of the removed element.

Step 6: Repeat step 5 until the queue is not empty and no vertex is left to be visited.

![breadth-first-search-in-graph-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/breadth-first-search-in-graph-data-structure.png)

### Depth-First Search or DFS

[DFS](https://www.simplilearn.com/tutorials/data-structure-tutorial/dfs-algorithm "DFS") is a search technique for finding a node in a graph data structure that meets a set of criteria.

* The depth-first search (DFS) algorithm traverses or explores data structures such as trees and graphs. The DFS algorithm begins at the root node and examines each branch as far as feasible before backtracking.
* To maintain track of the child nodes that have been encountered but not yet inspected, more memory, [generally a stack](https://www.simplilearn.com/tutorials/data-structure-tutorial/stacks-in-data-structures "generally a stack"), is required.

Algorithm of depth-first search

Step 1: Consider the graph you want to navigate.

Step 2: Select any vertex in our graph, say v1, from which you want to begin traversing the graph.

Step 3: Examine any two data structures for traversing the graph.

* Visited array (size of the graph)
* Stack data structure

Step 4: Insert v1 into the array's first block and push all the adjacent nodes or vertices of vertex v1 into the stack.

Step 5: Now, using the FIFO principle, pop the topmost element and put it into the visited array, pushing all of the popped element's nearby nodes into it.

Step 6: If the topmost element of the stack is already present in the array, discard it instead of inserting it into the visited array.

Step 7: Repeat step 6 until the stack data structure isn't empty.

![depth-first-search-in-graph-data-structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/depth-first-search-in-graph-data-structure.png)

You will now look at applications of graph data structures after understanding the graph traversal algorithm in this tutorial.

## Application of Graphs in Data Structures

Following  are some applications of graphs in data structures:

* Graphs are used in computer science to depict the flow of computation.
* Users on Facebook are referred to as vertices, and if they are friends, there is an edge connecting them. The Friend Suggestion system on Facebook is based on graph theory.
* You come across the Resource Allocation Graph in the Operating System, where each process and resource are regarded vertically. Edges are drawn from resources to assigned functions or from the requesting process to the desired resource. A stalemate will develop if this results in the establishment of a cycle.
* Web pages are referred to as vertices on the World Wide Web. Suppose there is a link from page A to page B that can represent an edge. This application is an illustration of a directed graph.
* Graph transformation systems manipulate graphs in memory using rules. Graph databases store and query graph-structured data in a transaction-safe, permanent manner.

Finally, in this tutorial, you’ll look at the code for the graphs in data structures

## Code Implementation of Graphs in Data Structures

| #include <stdio.h>#include<stdlib.h>#include <stdlib.h>#define V 6             // Define the maximum number of vertices in the graphstruct graph                    // declaring graph data structure{struct Node* point[V];     // An array of pointers to Node to represent an adjacency list};struct Node                     // declaring node{int destination;struct Node* next;};struct link                    // declaring edge{int source, destination;};struct graph* make_Graph(struct link edges[], int x)             // function to create graph{int i;struct graph* graph = (struct graph*)malloc(sizeof(struct graph));          // defining graphfor (i = 0; i < V; i++) {graph->point[i] = NULL;}for (i = 0; i < x; i++){int source = edges[i].source;int destination = edges[i].destination;struct Node* Node1 = (struct Node*)malloc(sizeof(struct Node));Node1->destination = destination;Node1->next = graph->point[source];graph->point[source] = Node1;}return graph;}void displayGraph(struct graph* graph)       // function to view garph{int i;for (i = 0; i < V; i++){struct Node* ptr = graph->point[i];while (ptr != NULL){printf("(%d —> %d)\t", i, ptr->destination);ptr = ptr->next;}printf("\n");}}int main(void){struct link edges[] ={{ 0, 1 }, { 1, 3 }, { 3, 0 }, { 3, 4 }, { 4, 5 }, { 5, 6 }};int n = sizeof(edges)/sizeof(edges[0]);struct graph *graph = make_Graph(edges, n);displayGraph(graph);return 0;} |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

Output

| (0 ù> 1)(1 ù> 3)(3 ù> 4)        (3 ù> 0)(4 ù> 5)(5 ù> 6)--------------------------------Process exited after 0.06697 seconds with return value 0Press any key to continue . . . |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

## FAQs

### 1. Where are graph data structures used in real life?

You most likely utilise social networking platforms such as Facebook, LinkedIn, Instagram, and others. A wonderful example of a graph in usage is social media. Graphs are used in social media to hold information about each user. Every user is a node in this case, just like in Graph. Similarly, Google Maps is another application that makes use of graphs. In the case of Google Maps, each place is referred to as a node, and the roads that connect them are referred to as edges.

### 2. What are the different types of graphs in data structure?

A graph is a non-linear data structure composed of nodes and edges. They come in a variety of forms. Namely, they are Finite Graphs, Infinite Graphs, Trivial Graphs, Simple Graphs, Multi Graphs, Null Graphs, Complete Graphs, Pseudo Graphs, Regular Graphs, Labeled Graphs, Digraph Graphs, Subgraphs, Connected or Disconnected Graphs, and Cyclic Graphs.

### 3. How many types of graphs are there in data structure?

They are of 14 to 15 types. However, the most commonly used graph is the finite graph.

### 4. What is a complete graph in data structure?

A graph is considered to be complete if there is an edge between every pair of vertices in the graph. In other words, all of the graph's vertices are connected to the remainder of the graph's vertices. A full graph of 'n' vertices has precisely nC2 edges and is written as Kn.

### 5. What is a directed acyclic graph?

A directed acyclic graph (DAG) is a graph that is directed and has no cycles linking the other edges in computer science and mathematics. This indicates that traversing the complete graph from one edge is impossible. The edges of the directed graph can only move in one direction. The graph is a topological sorting in which each node has a specific order.

### 6. What is graph in data structure?

A graph is a type of non-linear data structure made up of vertices and edges. Vertices are also known as nodes, while edges are lines or arcs that link any two nodes in the network. In more technical terms, a graph comprises vertices (V) and edges (E). The graph is represented as G(E, V).

### 7. What is graph in data structure and its application?

A graph is a non-linear data structure made up of vertices (or nodes) linked by edges (or arcs), which can be directed or undirected. Graphs are used in computer science to depict the flow of computation.

### 8. How are graphs useful when interpreting data?

Graphs are a popular way to visually depict data connections. A graph's objective is to convey too many or intricate facts to be fully expressed in words and in less space. However, do not use graphs for little quantities of data that may be expressed in a phrase.
