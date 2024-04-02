### Setting Up Environment
Reference: 
<br>[How to set up visual studio code for C and C++ programming 2021.](https://dev.to/narottam04/step-by-step-guide-how-to-set-up-visual-studio-code-for-c-and-c-programming-2021-1f0i)
<br>[How to Write And Run C and C++ Code in Visual Studio Code](https://www.freecodecamp.org/news/how-to-write-and-run-c-cpp-code-on-visual-studio-code/)

### Similarities & Differences between Java
Reading: [c-for-java-programmers](https://drive.google.com/file/d/1YpDcP5WyxiF6lyXFadFWXfSr8jSHgHi9/view)
- C doesn't have `boolean` variable; it uses **0** to represent **false**, and **any non-zero value** to represent **true**.
- `const` in C = `final` in java
- Array initialization
    - In java:  
      `int[] numbers;`  
      `int[] numbers = new int[3];`  
      `int[] numbers = {1, 2, 3};`
    - In C:  
      `int numbers[3];`  
      `int numbers[3] = {1, 2, 3};`
    - In C, you put the square brackets *after* the variable name and you have to know the size of the array *at compile-time*.
- Arrays and other reference types are often called **pointers** in C since they “point” to the data in memory.
- In C, there is *no way* to get the length of an array.
- In C, strings are arrays of chars.  
  `char name[] = "George";` - Don't have to specify the length of the array here
- In C, functions must be declared before they can be used. Use a **forward declaration** if need to define a function after its first use.
