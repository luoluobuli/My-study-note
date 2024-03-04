### Tree, binary tree, complete binary tree, full binary tree
* **Tree:** some connected nodes, no limits of the number of children  
* Data structure  
![image](images/Tree-1.png)

* **Binary tree:** a kind of tree that each node can have at most 2 children  
  **Leaf:** A tree node with no children  
  **Internal node:** A node with at least one child  
  **Parent:** A node with a child is said to be that child's parent. A node's **ancestors** include the node's parent, the parent's parent, etc., up to the tree's root  
  **Root:** The one tree node with no parent  
  **Height:** number of edges to the deepest node (4 in this example)  
  If only a root exists, the height is 0. If the tree is empty, the height can be 0 or -1.  
![image](images/Tree-3.png)  
* **Complete binary tree:** nodes are arranged from top to bottom, left to right
* **Full binary tree:** each node has two or no children
* **Perfect binary tree:** complete and full
![image](images/Tree-2.png)



### Heap
* A kind of **complete binary tree** that follows specific order.
* **Min heap:** a node's key <= its children's key. **Max heap:** a node's key >= its children's key.  
![image](images/Tree-4.png)
* **Storage:** array  
![image](images/Tree-5.png)
* If the current index is i and the array starts to store data at index 0,  
  **Parent's index:** ⌊i/2⌋  
  **Left child's index:** 2i  
  **Right child's index:** 2i+1  
* **Height:** O(logN)  

### Priority queue
* ADT
* **Underlying data structure:** heap
* A queue where each item has a priority, and items with higher priority are closer to the front of the queue than items with lower priority
* **Methods:**  
  `Enqueue(PQueue, x)` Inserts x after all equal or higher priority items (sort here)  
  `Dequeue(PQueue)`	Returns and removes the item at the front of PQueue (directly remove)  
* **Runtime complexity:**  
  enqueue: O(logN)  
  dequeue: O(logN)  
  peek: O(1)  
  isEmpty: O(1)  
  getLength: O(1)  

### Binary search tree (BST)
* A kind of **binary tree** that follows specific order.
