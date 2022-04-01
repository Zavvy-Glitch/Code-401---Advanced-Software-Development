# Stacks & Queues

## What is a Stack?
  - A stack is a data structure that consists of Nodes. Each Node references the next node in the stack, but does not reference the previous.

### Terminology
| Push - O(1) | POP - O(1) | Top - O(1) | Peek - O(1) | isEmpty - O(1) | FILO | LIFO |
|-------------|------------|------------|-------------|----------------|------|------|
| Nodes or items that are put into the stack are pushed. Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack. | Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised. Popping a Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.| This is the top of the stack. | When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised. When conducting a peek, you will only be inspecting the top Node of the stack. | returns true when stack is empty otherwise returns false | This means that the first item added in the stack will be the last item popped out of the stack. | This means that the last item added to the stack will be the first item popped out of the stack. | Nodes or items that are added to the queue. | Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised. |


## What is a Queue?
  - Is an ordered list of elements where an element is inserted at the end of the queue and is removed from the front of the queue.

### Terminology
| Enqueue - O(1) | Dequeue - O(1) | Front | Rear | Peek - O(1) | isEmpty - O(1) | FIFO | LILO |
|----------------|----------------|-------|------|-------------|----------------|------|------|
| Nodes or items that are added to the queue. If called when the queue is empty an exception will be raised. When you add an item to a queue, you use the enqueue action. This is done with an O(1) operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation. | Nodes or items that are removed from the queue. When you remove an item from a queue, you use the dequeue action. This is done with an O(1) operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the front Node of the queue. | This is the front/first Node of the queue. | This is the rear/last Node of the queue. | When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised. When conducting a peek, you will only be inspecting the front Node of the queue. | Returns true when queue is empty otherwise returns false. | This means that the first item in the queue will be the first item out of the queue. | This means that the last item in the queue will be the last item out of the queue. |
