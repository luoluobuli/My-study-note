### Bubble Sort
- Iterates through a list, comparing and swapping adjacent elements if the second element is less than the first element. Keep doing it until no swap happens in an iteration.  
![image](images/Sort-bubble.png)
```
BubbleSort(array, size) {
  for (i = 0; i < size - 1; i++) {
    for (j = 0; j < size - i - 1; j++) {
      if (array[j] > array[j+1]) {
        // Swap
        temp = array[j]
        array[j] = array[j + 1]
        array[j + 1] = temp
      } 
    }
  }
}
```
- **Runtime:** *all cases:* **O(N^2)**  
  *Outer loop:* **N** | *Inner loop:* **N-1** | *Total:* **N(N-1)**

### Selection Sort
-  Treats the input as two parts, a sorted part and an unsorted part, and repeatedly selects the proper next value to move from the unsorted part to the end of the sorted part.  
![image](images/Sort-selection2.png)
```
SelectionSort(array, size) {
   i = 0
   j = 0
   indexSmallest = 0
   temp = 0  // Temporary variable for swap
   
   for (i = 0; i < size - 1; ++i) {
      
      // Find index of smallest remaining element
      indexSmallest = i
      for (j = i + 1; j < size; ++j) {
         
         if ( array[j] < array[indexSmallest] ) {
            indexSmallest = j
         }
      }
      
      // Swap array[i] and array[indexSmallest]
      temp = array[i]
      array[i] = array[indexSmallest]
      array[indexSmallest] = temp
   }
}
```
- **Runtime:** *all cases:* **O(N^2)**  
  *Outer loop:* **N-1** | *Inner loop:* **N/2** | *Total:* **(N-1)N/2**
- The minimum number of assigning indexSmallest:
  **N** *(in total)* | **N-1** *(inside loop)*

### Insertion Sort
- Treats the input as two parts, a sorted part and an unsorted part, and repeatedly inserts the next value from the unsorted part into the correct location in the sorted part.
- **Difference from Selection Sort:** Selection: find the smallest then sort; Insersion: get elements from the unsorted part in order, place them in the sorted part.  
![image](images/Sort-insertion.png)
```
InsertionSort(array, size) {
   i = 0
   j = 0
   temp = 0  // Temporary variable for swap
   
   for (i = 1; i < size; ++i) {
      j = i
      // Insert array[i] into sorted part
      // stopping once array[i] in correct position
      while (j > 0 && array[j] < array[j - 1]) {
         // Swap array[j] and array[j - 1]
         temp = array[j]
         array[j] = array[j - 1]
         array[j - 1] = temp
         --j
      }
   }
}
```
- **Runtime:** **O(N^2)** *or* **O(N)**  
  In-order array: If there C of unsorted elements, *sorted elements:* **N-C-1** | *unsorted elements:* **O(C*N)** | *overall runtime:* **O(N)**  
  Reversed array: *outer loop:* **N-1** | *inner loop:* **N/2** | *Total:* **N(N-1)**  
  Other cases: In between
  
### Heap Sort
- **Heapify:** The internal node with the largest index -> the root node at index 0
  - the largest internal node index is **(N div 2) - 1**  
  ![image](Sort-heap.png)
- **Heapsort:** Repeatedly removes the maximum value, stores that value at the end index, and decrements the end index. The removal loop repeats until the end index is 0.
```
Heapsort(numbers, numbersSize) {
  // Heapify numbers array
  for (i = numbersSize / 2 - 1; i >= 0; i--) {
    MaxHeapPercolateDown(i, numbers, numbersSize)
  }
  
  for (i = numbersSize - 1; i > 0; i--) {
    Swap numbers[0] and numbers[i]
    MaxHeapPercolateDown(0, numbers, i)
  }
}
```

### Merge Sort
```
Merge(numbers, i, j, k) {
   mergedSize = k - i + 1                // Size of merged partition
   mergePos = 0                          // Position to insert merged number
   leftPos = 0                           // Position of elements in left partition
   rightPos = 0                          // Position of elements in right partition
   mergedNumbers = new int[mergedSize]   // Dynamically allocates temporary array
                                         // for merged numbers
   
   leftPos = i                           // Initialize left partition position
   rightPos = j + 1                      // Initialize right partition position
   
   // Add smallest element from left or right partition to merged numbers
   while (leftPos <= j && rightPos <= k) {
      if (numbers[leftPos] <= numbers[rightPos]) {
         mergedNumbers[mergePos] = numbers[leftPos]
         ++leftPos
      }
      else {
         mergedNumbers[mergePos] = numbers[rightPos]
         ++rightPos
         
      }
      ++mergePos
   }
   
   // If left partition is not empty, add remaining elements to merged numbers
   while (leftPos <= j) {
      mergedNumbers[mergePos] = numbers[leftPos]
      ++leftPos
      ++mergePos
   }
   
   // If right partition is not empty, add remaining elements to merged numbers
   while (rightPos <= k) {
      mergedNumbers[mergePos] = numbers[rightPos]
      ++rightPos
      ++mergePos
   }
   
   // Copy merge number back to numbers
   for (mergePos = 0; mergePos < mergedSize; ++mergePos) {
      numbers[i + mergePos] = mergedNumbers[mergePos]
   }
}
```
```
MergeSort(numbers, i, k) {
   j = 0
   
   if (i < k) {
      j = (i + k) / 2  // Find the midpoint in the partition
      
      // Recursively sort left and right partitions
      MergeSort(numbers, i, j)
      MergeSort(numbers, j + 1, k)
      
      // Merge left and right partition in sorted order
      Merge(numbers, i, j, k)
   }
}
```
