# Trees

| Terminology | Definitions |
| ----------- | ----------- |
| Node | A Tree node is a component which may contain it’s own values, and references to other nodes |
| Root | The root is the node at the beginning of the tree |
| K | A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, `k = 2` |
| Left | A reference to one child node in a binary tree |
| Right | A Reference to the other child node in a binary tree |
| Edge | The edge in a tree is the link between a parent and child node |
| Leaf | Is a node that does not have any children |
| Height | Number of edges from the root to the furthest leaf is the height of the tree |

## Traversals
  - Two aspects of how to traverse a tree
      - Depth First
      -  Breadth First

  ### Depth First 
      -   Traverses by prioritizing the depth/height of the tree.
          - This can be accomplished in three methods
            - Pre Order: `root` -> `left` -> `right`
                - 
                   ALGORITHM preOrder(root)
                  INPUT <-- root node
                  OUTPUT <-- pre-order output of tree node's values

                  OUTPUT <-- root.value

                  if root.left is not Null
                    preOrder(root.left)

                  if root.right is not NULL
                    preOrder(root.right)

                - `root` must be looked at first then we iterate through our function going left then right
         
            - In Order: `left` -> `root` -> `right`
              -   
                  ALGORITHM inOrder(root)
                  // INPUT <-- root node
                  // OUTPUT <-- in-order output of tree node's values

                  if root.left is not NULL
                    inOrder(root.left)

                  OUTPUT <-- root.value

                  if root.right is not NULL
                    inOrder(root.right)
        
            - Post Order: `left` -> `right` -> `root`
              -   
                  ALGORITHM postOrder(root)
                  // INPUT <-- root node
                  // OUTPUT <-- post-order output of tree node's values

                  if root.left is not NULL
                    postOrder(root.left)

                  if root.right is not NULL
                    postOrder(root.right)

                  OUTPUT <-- root.value
                  
          - Most commonly traversed by using recursion which relies on a call stack to navigate back up the tree when the end is reached.

  ### Breadth First
    -   Traverses the tree node by node
    -   Utilizes enqueue and dequeue
         - 
                  ALGORITHM breadthFirst(root)
                  // INPUT  <-- root node
                  // OUTPUT <-- front node of queue to console

                  Queue breadth <-- new Queue()
                  breadth.enqueue(root)

                  while breadth.peek()
                    node front = breadth.dequeue()
                    OUTPUT <-- front.value

                  if front.left is not NULL
                    breadth.enqueue(front.left)

                  if front.right is not NULL
                    breadth.enqueue(front.right)
