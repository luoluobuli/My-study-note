### Stack
**What is it:** abstract data type (ADT)  
**Feature:** first in, last out (push on the top, pop at the top)  
**Underlying data structure:** ? 

### Queue
**What is it:** ADT  
**Feature:** first in, first out (enqueue at the end, dequeue at the front)  
**Underlying data structure:** ?

### Deque
**What is it:** ADT  
**Feature:** double-sided queue, can push and pop at the front and the end  
**Underlying data structure:** ?

### Depth First Search (DFS)
**Implementation:** Stack  
**Traversal algorithm:**
```
DFS(startV) {
   Push startV to stack

   while ( stack is not empty ) {
      currentV = Pop stack
      if ( currentV is not in visitedSet ) {
         "Visit" currentV
         Add currentV to visitedSet
         for each vertex adjV adjacent to currentV
            Push adjV to stack
      }
   }
}
```

### Breadth First Search (BFS)  
**Implementation:** Queue  
**Traversal algorithm:**  
```
BFS(startV) {
   Enqueue startV in frontierQueue
   Add startV to discoveredSet

   while ( frontierQueue is not empty ) {
      currentV = Dequeue from frontierQueue
      "Visit" currentV
      for each vertex adjV adjacent to currentV {
         if ( adjV is not in discoveredSet ) {
            Enqueue adjV in frontierQueue
            Add adjV to discoveredSet
         }
      }
   }
}
```
