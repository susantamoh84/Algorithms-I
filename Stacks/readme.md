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
  

