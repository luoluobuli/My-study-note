### List
- **Type:** ADT
- **Comman operations:**  
![image](images/List1.png)

### ArrayList
- **Type:** data structure
- **Underlying data structure:** array
- **Instance:** `Object[] array`, `int length`
- **Methods:**
  - Note: **length** = the number of valid elements in the array; **array.length** = the capacity of the array.
  - Resize
    ```
    resize(list, newCapacity) {
       newArray = new Object[newCapacity]
       Copy all elements from list.array to newArray
       list.array = newArray
    }
    ```
  - Append
    ```
    append(list, newItem) {
       if (list.array.length == list.length) {
          resize(list, list.length * 2)
       }
       list.array[list.length] = newItem
       list.length = list.length + 1
    }
    ```
  - Prepend
    ```
    prepend(list, newItem) {
       if (list.array.length == list.length) {
          resize(list, list.length * 2)
       }
        // Shift every element one index right
       for (i = list.length; i > 0; i--) {
          list.array[i] = list.array[i - 1]
       }
       list.array[0] = newItem
    }
    ```
  - InsertAfter
    ```
    insertAfter(list, index, newItem) {
       if (list.array.length == list.length) {
          resize(list, list.length * 2)
       }
        // Shift every element after the given index one index right
       for (i = list.length; i > index + 1; i--) {
          list.array[i] = list.array[i - 1]
       }
       list.array[index + 1] = newItem
       list.length = list.length + 1
    }
    ```
  - Search
    ```
    search(list, item) {
       for (i = 0; i < list.length; i++) {
          if (list.array[i] == item) {
             return i
          }
       }
       return -1 // not found
    }
    ```
  - RemoveAt
    ```
    removeAt(list, index) {
       if (index >= 0 && index < list.length) {
          // Shift every element from given index one index left
          for (i = index; i < list.length - 1; i++) {
             list.array[i] = list.array[i + 1]
          }
          list.length = list.length - 1
       }
    }
    ```

### Singly-Linked list
- **Type:** data structure
- **Underlying data structure:** N/A
- **Nested class:** `Node`
- **Instance:** `Node head`, `Node tail`, `int size`
- **Methods:**
    - Append
      ```
      append(list, newNode) {
          // When list is empty
         if (list.head == null) {
            list.head = newNode
            list.tail = newNode
         } else {
            list.tail.next = newNode
            list.tail = newNode
         }
      }
      ```
