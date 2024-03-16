- **Common compile errors:**
  - ```
    public static void main(String[] args) {
      Generics<T> test = new Generics<T>;
    }
    ```
    Can't create new generic type in the runtime!
  - `T test = new T`
  - `T[] test = new T[10]`  
    Can't directly create an object/an array with elements of the type!
- **Correct way to create a generic type:**
  - `T[] test = (T[])new Object[10]`
