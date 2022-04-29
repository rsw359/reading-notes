# Stacks and Queues

## What is a Stack

A stack is a data structure that consists of **`Nodes`**. Each **`Node`** references the next Node in the stack, but does not reference its previous.

### FILO

**F**irst **I**n **L**ast **O**ut

This means that the first item added in the stack will be the last item popped out of the stack.

### LIFO

**L**ast **I**n **F**irst **O**ut

This means that the last item added to the stack will be the first item popped out of the stack.

### Push O(1)

Pushing a Node onto a stack will always be an **`O(1)`** operation. This is because it takes the same amount of time no matter how many Nodes (**`n`**) you have in the stack.

When adding a Node, you **`push`** it into the stack by assigning it as the new top, with its **`next`** property equal to the original **`top`**.

```python
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node
```

### Pop O(1)

Popping a Node off a stack is the action of removing a Node from the top. When conducting a **`pop`**, the **`top`** Node will be re-assigned to the Node that lives below and the **`top`** Node is returned to the user.

Typically, you would check **`isEmpty`** before conducting a **`pop`**

```python
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value
```

### Peek O(1)

When conducting a **`peek`**, you will only be inspecting the **`top`** Node of the stack.

Typically, you would check **`isEmpty`** before conducting a **`peek`**

We do not re-assign the **`next`** property when we **`peek`**
 because we want to keep the reference to the next Node in the stack.

```python
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   return top.value
```

### **IsEmpty O(1)**

```python
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL
```

## **What is a Queue**

A queue is a data structure that follows these concepts:

### FIFO

**F**irst **I**n **F**irst **O**ut

This means that the first item in the queue will be the first item out of the queue.

### LILO

**L**ast **I**n **L**ast **O**ut

This means that the last item in the queue will be the last item out of the queue.

### Enqueue O(1)

When you add an item to a queue, you use the **`enqueue`** action. This is done with an **`O(1)`** operation in time because it does not matter how many other items live in the queue (**`n`**); it takes the same amount of time to perform the operation.

```python
ALGORITHM enqueue(value)
// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
   node = new Node(value)
   rear.next <-- node
   rear <-- node
```

### Dequeue O(1)

When you remove an item from a queue, you use the **`dequeue`** action. This is done with an **`O(1)`** operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the **`front`** Node of the queue

Typically, you would check **`isEmpty`** before conducting a **`dequeue`**

```python
ALGORITHM dequeue()
// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty

   Node temp <-- front
   front <-- front.next
   temp.next <-- null

   return temp.value
```

### Peek O(1)

When conducting a **`peek`**, you will only be inspecting the **`front`** Node of the queue.

Typically, you want to check **`isEmpty`** before conducting a **`peek`**

```python
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of the front Node in Queue
// EXCEPTION if Queue is empty

   return front.value
```

### **IsEmpty O(1)**

```python
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL
```