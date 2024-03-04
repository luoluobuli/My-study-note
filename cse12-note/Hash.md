### Hash Tables
**What is it:** data structure  
**Underlying data structure:** array  
When mapped to a hash table, each element will be given a **key** by a **hash function**, and be assigned to a bucket with specific index.  
The hash function guarantees that the same element will be given the same key, but different elements may also get the same key.

**Collision**: an item being inserted into a hash table maps to the same bucket as an existing item in the hash table.  
To solve collision, there are 2 methods.  
1. Chaining
   
3. Linear probing
