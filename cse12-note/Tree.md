### Tree, binary tree, complete binary tree, full binary tree
* **Tree:** some connected nodes, no limits of the number of children  
![image](images/Tree-1.png)

* **Binary tree:** a kind of tree that each node can have at most 2 children  
* **Complete binary tree:** nodes are arranged from top to bottom, left to right
* **Full binary tree:** each node has two or no children
* **Perfect binary tree:** complete and full
![image](images/Tree-2.png)

* **Leaf:** node that has no child
* **Height:** number of edges to the deepest node (4 in this example)  
  If only a root exists, the height is 0. If the tree is empty, the height can be 0 or -1.  
![image](images/Tree-3.png)  


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
