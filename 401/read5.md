# Linked Lists

## Refrences
* https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d
* https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996
* https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html


## what is a linked list? 
* A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

1. Linked List - A data structure that contains nodes that links/points to the next node in the list.
2. Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
3. Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
4. Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
5. Next - Each node contains a property called Next. This property contains the reference to the next node.
6. Head - The Head is a reference type of type Node to the first node in a linked list.
7. Current - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

## Traversal 

* The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.

## Big O 

* Big O Notation is a way of evaluating the performance of an algorithm.

* The Big O of time for Includes would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list.

* The Big O of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.

## what is a node anyway 

* Print Out Nodes - 
Printing out all of the nodes in a Linked List is very similar to what we did in the Find() method. This is because we are leveraging our Current node and a while loop to traverse through the existing linked list.

* A node only knows about what data it contains, and who its neighbor is.
