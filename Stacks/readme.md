# Stacks and Queues

  - Operations: insert, remove, iterate, test if empty
  - Stack: LIFO = Last in first out
  - Queue: FIFO = first in first out
  
# Client, Implementationm interface:

  - Seperate interface and implementation
  - Benefits:
    - Client doesn't know details of implementation => many implementations to choose from
    - Implementation doesn't details about clients

# Stack methods:

  - push(Object item)
  - pop()
  - isEmpty()
  - size()
  
# Stack array implementation:

  - push(): add new item at s[N]
  - pop(): remove item from s[N-1]
  - Stack overflows when N exceeds capacity
  
# Resizing Arrays:

  - amoratized analysis: Cost of inserting first N items: N + (2+4+6....+N) ~3N
    - Total cost averaged over all operations
    
  - Less waisted space
  - Every operation takes constant amortized time.
  
  - faster compared to linkedlist implementation
  - Number of array resizing is lgN - very decent

# LinkedList implementation:

  - Every operation takes constant time in worst case
  - Uses extra time and space to deal with links
  
# Queue

  - apis same as Stack:
  - enqueue(Object object)
  - dequeue()
  - isEmpty()
  - size()
  
# LinkedList Implementation:

  - 2 pointers - first & last item in the list
  - dequeue - remove first element and change the first pointer
  - enqueue - add new item in the last and change the last pointer
  
  - Linear time for enqueue
  - Constant time for dequeue
  
# Resizing Array implementation:

  - enqueue(): add new item at q[tail]
  - dequeue(): remove item from q[head]
  - Update head and tail modulo the capacity
  - add resizing array
  
# Applications:

  - Make a recursive program non-recursive
  - Arithmetic expression evaluation
    - Two Stack algorithm
      - value stack
      - operation stack
      - When encountered with right paranthesis:
        - Apply opearator to the top 2 element and put the value back in the value stack
      - When encountered with left paranthesis:
        - Do nothing. Skip

# Interview questions:

  - Queue with two stacks. Implement a queue with two stacks so that each queue operations takes a constant amortized number of stack operations.
  - Stack with max. Create a data structure that efficiently supports the stack operations (push and pop) and also a return-the-maximum operation. Assume the elements are real numbers so that you can compare them.
  - Java generics. Explain why Java prohibits generic array creation.


