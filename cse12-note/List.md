### List
- **Type:** ADT
- **Comman operations:**  
![image](images/List1.png)

### ArrayList
- **Type:** data structure
- **Underlying data structure:** array
- **Instance:** `Object[] array`, `int size`
- **Methods:**
  - Note: size = the number of valid elements in the array; length = the capacity of the array.
  - Append
    ```
    ArrayListAppend(list, newItem) {
       if (list.size == list.length) {
          ArrayListResize(list, list.length * 2)
       }
       list.array[list.length] = newItem
       list.length = list.length + 1
    }
    ```
  - Resize
    ```
    ArrayListResize(list, newSize) {
       newArray = new Object[newSize]
       Copy all elements from list.array to newArray
       list.array = newArray
       list.size = newSize
    }
    ```

### Singly-Linked list
