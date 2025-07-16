## Java Coding Interview Question: Sorting Without Streams (Facade Pattern Required)

**Question:**  
Write a Java method that takes an array of integers as input and returns a new array containing the same integers sorted in ascending order.  
**You are not allowed to use the Java Stream API or any built-in Java sorting methods (such as `Arrays.sort()`, `Collections.sort()`, or similar).**  
You may use only basic Java language constructs, such as loops, arrays, and conditionals.

**Additional Requirement:**  
You must implement your sorting logic using the **Facade Pattern**.  
Your solution should define a Facade class that provides a simple interface for sorting, while internally it may use one or more classes to perform the actual sorting logic.

**Hints:**  
- The Facade class could be named `SortFacade` with a method such as `sort(int[] input)`.
- Inside the Facade, you might define separate classes for different sorting algorithms, e.g., `BubbleSort`, `QuickSort`, `MergeSort`, etc.
- The Facade can decide which algorithm to use, or always use one (for example, always use `QuickSort`).
- The user of the Facade should only interact with the Facade's public method, not the internal sorting classes directly.
- You do **not** need to implement more than one sorting algorithm, but your design should make it easy to add more algorithms in the future if desired.
- Your main method (or test code) should create an instance of the Facade and call its sort method, not the helper classes.

**Function Signature:**  
```java
public static int[] sortArray(int[] input)
```

**Example:**  
```java
Input: [4, 2, 7, 1, 3]
Output: [1, 2, 3, 4, 7]
```

**Constraints:**
- Do not use the Java Stream API.
- Do not use built-in sorting methods.
- You must use the Facade design pattern in your implementation.
- Your solution should have a time complexity better than O(n²) if possible.
- Provide both the code and a brief explanation of how you applied the Facade pattern.
