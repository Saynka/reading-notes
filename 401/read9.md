# Stacks and Queues

## refrences

- https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html

### 2 types stacks

1. FILO "First In Last Out" - This means that the first item added in the stack will be the last item popped out of the stack.
2. LIFO "Last In First Out" - This means that the last item added to the stack will be the first item popped out of the stack.

## Terms

1. Push - Nodes or items that are put into the stack are pushed

- ALOGORITHM push(value)
  - // INPUT <-- value to add, wrapped in Node internally
  - // OUTPUT <-- none
  - node = new Node(value)
  - node.next <-- Top
  - top <-- Node

2. Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.

- ALGORITHM pop()

  - // INPUT <-- No input
  - // OUTPUT <-- value of top Node in stack

  * // EXCEPTION if stack is empty

  * Node temp <-- top
  * top <-- top.next
  * temp.next <-- null
    - return temp.value

3. Top - This is the top of the stack.

4. Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.

- ALGORITHM peek()

  - // INPUT <-- none
  - // OUTPUT <-- value of top Node in stack
  - // EXCEPTION if stack is empty

    - return top.value

5. IsEmpty - returns true when stack is empty otherwise returns false.

- ALGORITHM isEmpty()

  - // INPUT <-- none
  - // OUTPUT <-- boolean

    - return top = NULL

## 2 types Queues

1. FIFO "First In First Out" - This means that the first item in the queue will be the first item out of the queue.
2. LILO "Last In Last Out" - This means that the last item in the queue will be the last item out of the queue.

## what is a queue

1. Enqueue - Nodes or items that are added to the queue.

- ALGORITHM enqueue(value)
  - // INPUT <-- value to add to queue (will be wrapped in Node internally)
  - // OUTPUT <-- none
  - node = new Node(value)
  - rear.next <-- node
  - rear <-- node

2. Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.

- ALGORITHM dequeue()

  - // INPUT <-- none
  - // OUTPUT <-- value of the removed Node
  - // EXCEPTION if queue is empty

  - Node temp <-- front
  - front <-- front.next
  - temp.next <-- null

    - return temp.value

3. Front - This is the front/first Node of the queue.
4. Rear - This is the rear/last Node of the queue.
5. Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.

- ALGORITHM peek()

  - // INPUT <-- none
  - // OUTPUT <-- value of the front Node in Queue
  - // EXCEPTION if Queue is empty

    - return front.value

6. IsEmpty - returns true when queue is empty otherwise returns false.

- ALGORITHM isEmpty()

  - // INPUT <-- none
  - // OUTPUT <-- boolean

    - return front = NULL
