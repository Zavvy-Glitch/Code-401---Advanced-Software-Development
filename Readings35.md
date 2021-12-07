# Graphs

- What is a graph?
  - A non-linear data structure that can be looked at as a collection of `vertices`(`nodes`) potentially connected by line segments and `edges`

## Terminology
|Vertex|Edge|Neighbor|Degree|
|------|----|--------|------|
|A vertex, also called a `node`, is a data object that can have zero or more adjacent vertices|An edge is a connection between two nodes|The neighbors of a node are its adjacent nodes, i.e., are connected via an edge|The degree of a vertex is the number of edges connected to that vertex|

### Undirected vs Directed Graphs

- Undirected Graphs:
  - A graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.
- Directed Graphs:
  - AKA: Digraph - a graph where every edge is directed. Each node is directed at another node with a specific requirement of what node should be referenced next.

### Complete - vs - Connected - vs - Disconnected

- Complete: a graph where all nodes are connected to all other nodes
- Connected: a graph where all `vertices`/`nodes` have atleast one edge
- Disconnected: a graph where some `vertices` do not or may not have an edge

### Acyclic vs Cyclic
  ** Cycle = when a node can be traversed through and potentially end up back at itself **
- Acyclic: directed graph without cycles.
- Cyclic: graph that has cycles. The path traversed starts and ends with the same vertex.

### Graph Representation
  - Graphs are represented through:
    - Adjacency Matrix
    - Adjacency List

* Adjacency Matrix: represented through a 2 dimensional array. 
  * (n)`vertices`=`n`x`n` Boolean matrix
  * Each row / column represent each vertex of the data structure.
    * Sparse: graph with very few connections
    * Dense: graph with many connections
* Adjacency List: most common way to represent graphs  
  * A collection of linked lists / array that lists all connected vertices

### Weighted Graphs
- a graph with numbers assigned to the edges. These numbers are called weights.
- This graph is integrated with Matrix / List Adjacencies

### Traversals
- Breadth First: is when you visit all the nodes that are closest to the root as possible. From there you traverse outwards, level by level, until you have visited all the vertices/nodes
  - Starts at a specific vertex/node
  - Traversing a graph with cycles will result in an infinite loop
  - Will need conditions to keep track of vertices that have already been visited
    - Algorithm
      - `Enqueue` the declared start node into the queue
      - Create a loop that will run while the node still has other nodes present
      - `Dequeue` the first node from the queue
      -  If the `Dequeue`'d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.
 
 - Depth First: uses a stack for traversal
   - Differs from traversing a tree
     - Algorithm
        - `Push` the root node into stack
        - Use a while loop while stack is not empty
        - `Peek` at the top node in stack
        - If top node has unvisitied children, mark the top node as visited, then `Push` any unvisited children back into stack
        - If top node does not have unvisited children, `Pop` that node from stack
        - Repeat until stack is empty

#### Real World Uses of Graphs
- GPS and Mapping
- Driving Directions
- Social Networks
- Airline Traffic
- Netflix uses graphs for suggestions of products
