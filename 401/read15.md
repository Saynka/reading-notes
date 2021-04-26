# Trees

## refrences

- https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html

## Vocabulary

- Node - A Tree node is a component which may contain it’s own values, and references to other nodes

- Root - The root is the node at the beginning of the tree

- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.

- Left - A reference to one child node, in a binary tree

- Right - A reference to the other child node, in a binary tree

- Edge - The edge in a tree is the link between a parent and child node

- Leaf - A leaf is a node that does not have any children

- Height - The height of a tree is the number of edges from the root to the furthest leaf

## pre-oder

ALGORITHM preOrder(root)
// INPUT <-- root node
// OUTPUT <-- pre-order output of tree node's values

    OUTPUT <-- root.value

    if root.left is not Null
        preOrder(root.left)

    if root.right is not NULL
        preOrder(root.right)

## in-order

ALGORITHM inOrder(root)
// INPUT <-- root node
// OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)

## post-order

ALGORITHM postOrder(root)
// INPUT <-- root node
// OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value

## pseudocode

ALGORITHM breadthFirst(root)
// INPUT <-- root node
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

## psuedocode

ALGORITHM breadthFirst(root)
// INPUT <-- root node
// OUTPUT <-- front node of queue to console

Queue breadth <-- new Queue()
breadth.enqueue(root)

while breadth.peek()
node front = breadth.dequeue()
OUTPUT <-- front.value

    for child in front.children
        breadth.enqueue(child)

## Big O

- The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.

- The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.
