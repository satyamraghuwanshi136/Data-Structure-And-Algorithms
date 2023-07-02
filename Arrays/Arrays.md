ARRAY DATA STRUCTURE

What is Array in Data Structure?
================================

-   An array is a linear data structure used for storing a collection of elements of the same data type.

-   An array is a data structure for storing more than one data item with a similar data type. 

-   The elements of an array are stored at contiguous memory locations.

-   The elements of an array are accessed using an index.

Why do we need Array Data Structure? 
=====================================

-   Storing multiple values of the same data type
    ---------------------------------------------

Arrays are useful for storing multiple values of the same data type, such as a list of integers or a series of characters. Without arrays, you would need to use multiple variables to store these values, which can be cumbersome and inefficient.

-   Accessing elements by index
    ---------------------------

Arrays provide a convenient way to access elements by their index, which makes it easy to retrieve, modify, or delete specific elements in the array.

-   Improving performance and memory usage
    --------------------------------------

Because arrays store elements in contiguous memory locations, they can be accessed quickly and efficiently using the index of the element. This makes it faster and more efficient to perform operations on the elements of the array, compared to other data structures such as linked lists or trees.

-   Implementing algorithms and data structures
    -------------------------------------------

Arrays are a fundamental building block of many algorithms and data structures, such as sorting algorithms, search algorithms, and stacks and queues. Using arrays can make these algorithms and data structures more efficient and easier to implement.

-   Interfacing with other programs and systems
    -------------------------------------------

Many programming languages and systems use arrays to represent data structures, such as matrices in linear algebra, or image data in computer graphics. Using arrays can make it easier to interface with these systems and perform operations on the data.

Applications of Array Data Structure:
=====================================

Below are some applications of arrays.

-   Storing and accessing data: Arrays are used to store and retrieve data in a specific order. For example, an array can be used to store the scores of a group of students, or the temperatures recorded by a weather station.

-   Sorting: Arrays can be used to sort data in ascending or descending order. Sorting algorithms such as bubble sort, merge sort, and quicksort rely heavily on arrays.

-   Searching: Arrays can be searched for specific elements using algorithms such as linear search and binary search.

-   Matrices: Arrays are used to represent matrices in mathematical computations such as matrix multiplication, linear algebra, and image processing.

-   Stacks and queues: Arrays are used as the underlying data structure for implementing stacks and queues, which are commonly used in algorithms and data structures.

-   Graphs: Arrays can be used to represent graphs in computer science. Each element in the array represents a node in the graph, and the relationships between the nodes are represented by the values stored in the array.

-   Dynamic programming: Dynamic programming algorithms often use arrays to store intermediate results of subproblems in order to solve a larger problem.

Real-Time Applications of Array:
================================

Below are some real-time applications of arrays.

-   Signal Processing: Arrays are used in signal processing to represent a set of samples that are collected over time. This can be used in applications such as speech recognition, image processing, and radar systems.

-   Multimedia Applications: Arrays are used in multimedia applications such as video and audio processing, where they are used to store the pixel or audio samples. For example, an array can be used to store the RGB values of an image.

-   Data Mining: Arrays are used in data mining applications to represent large datasets. This allows for efficient data access and processing, which is important in real-time applications.

-   Robotics: Arrays are used in robotics to represent the position and orientation of objects in 3D space. This can be used in applications such as motion planning and object recognition.

-   Real-time Monitoring and Control Systems: Arrays are used in real-time monitoring and control systems to store sensor data and control signals. This allows for real-time processing and decision-making, which is important in applications such as industrial automation and aerospace systems.

-   Financial Analysis: Arrays are used in financial analysis to store historical stock prices and other financial data. This allows for efficient data access and analysis, which is important in real-time trading systems.

-   Scientific Computing: Arrays are used in scientific computing to represent numerical data, such as measurements from experiments and simulations. This allows for efficient data processing and visualization, which is important in real-time scientific analysis and experimentation.

==

Advantages of array data structure:
===================================

-   Efficient access to elements: Arrays provide direct and efficient access to any element in the collection. Accessing an element in an array is an O(1) operation, meaning that the time required to access an element is constant and does not depend on the size of the array.

-   Fast data retrieval: Arrays allow for fast data retrieval because the data is stored in contiguous memory locations. This means that the data can be accessed quickly and efficiently without the need for complex data structures or algorithms.

-   Memory efficiency: Arrays are a memory-efficient way of storing data. Because the elements of an array are stored in contiguous memory locations, the size of the array is known at compile time. This means that memory can be allocated for the entire array in one block, reducing memory fragmentation.

-   Versatility: Arrays can be used to store a wide range of data types, including integers, floating-point numbers, characters, and even complex data structures such as objects and pointers.

-   Easy to implement: Arrays are easy to implement and understand, making them an ideal choice for beginners learning computer programming.

-   Compatibility with hardware: The array data structure is compatible with most hardware architectures, making it a versatile tool for programming in a wide range of environments.

==


Disadvantages of array data structure:
======================================

-   Fixed size: Arrays have a fixed size that is determined at the time of creation. This means that if the size of the array needs to be increased, a new array must be created and the data must be copied from the old array to the new array, which can be time-consuming and memory-intensive.

-   Memory allocation issues: Allocating a large array can be problematic, particularly in systems with limited memory. If the size of the array is too large, the system may run out of memory, which can cause the program to crash.

-   Insertion and deletion issues: Inserting or deleting an element from an array can be inefficient and time-consuming because all the elements after the insertion or deletion point must be shifted to accommodate the change.

-   Wasted space: If an array is not fully populated, there can be wasted space in the memory allocated for the array. This can be a concern if memory is limited.

-   Limited data type support: Arrays have limited support for complex data types such as objects and structures, as the elements of an array must all be of the same data type.

-   Lack of flexibility: The fixed size and limited support for complex data types can make arrays inflexible compared to other data structures such as linked lists and trees.

For programming references refer to Java Notes for Professionals by Goalkicker

Use Interview Bit for Interview Guide and cheatsheets

Algorithms and Questions
========================

-   kadane's algorithm
    ------------------

Subarray: A subarray is a contiguous portion of an array. In other words, it is a consecutive sequence of elements selected from an array without changing the order of the remaining elements.

We know that an array is a contiguous memory block. Similarly, a sub-array is any contiguous part of that array, which may consist of any number of elements with at least one element in it.

Let us write all the subarrays for the array: ['a','b','c','d']

The sub-arrays for this array are:

Index of element  Subarrays possible
```java
0 -> 'a'  {'a'}, {'a', 'b'}, {'a', 'b', 'c'}, {'a', 'b', 'c', 'd'}

1 -> 'b'  {'b'}, {'b', 'c'}, {'b', 'c', 'd'}

2 -> 'c'  {'c'}, {c', 'd'}

3 -> 'd'  {'d'}
```
Total number of subarrays possible in an array of length N = N.(N+1)/2

## **Algorithm:**

Kadane's Algorithm is an iterative dynamic programming algorithm. It calculates the maximum sum subarray ending at a particular position by using the maximum sum subarray ending at the previous position. 

The idea of Kadane's algorithm is to maintain a maximum subarray sum ending at every index 'i' of the given array and update the maximum sum obtained by comparing it with the maximum sum of the subarray ending at every index 'i'

Follow the below steps to solve the problem.

-   Define two-variable currSum which stores maximum sum ending here and maxSum which stores maximum sum so far.

-   Initialize currSum with 0 and maxSum with INT_MIN.

-   Now, iterate over the array and add the value of the current element to currSum and check

-   If currSum is greater than maxSum, update maxSum equals to currSum.

-   If currSum is less than zero, make currSum equal to zero.

-   Finally, print the value of maxSum.

## **Pseudocode:**
```java
function Kadane(arr, N)

    // Initializing curSum to 0 and maxSum to min value, denoting an empty subarray

    curSum =  0

    maxSum =  INT_MIN

    for idx =  0 to N-1

      curSum = curSum + arr[idx] // Taking the max of maxSum and the curSum of the subarray

      maxSum =  max(maxSum, curSum)

        // Checking if the curSum becomes negative

    if curSum <  0

      curSum =  0

    return maxSum
```
Time complexity: O(N), where N is the number of elements in the array, as we traverse the array once to get the maximum subarray sum.

Space complexity: O(1), as no extra space is required.

* * * * *

## **Que 1: Maximum Subarray Sum**

Links: [Leetcode](https://leetcode.com/problems/maximum-subarray/)

* * * * *

### **Solution:**

-   Define two-variable currSum which stores maximum sum ending here and maxSum which stores maximum sum so far.

-   Initialize currSum with 0 and maxSum with INT_MIN.

-   Now, iterate over the array and add the value of the current element to currSum and check

    -   If currSum is greater than maxSum, update maxSum equals to currSum.

    -   If currSum is less than zero, make currSum equal to zero.

-   Finally, print the value of maxSum.

* * * * *

## **Que 2: Flip Bits**

Links: [codingninja1](https://www.codingninjas.com/studio/guided-paths/data-structures-algorithms/content/118820/offering/1381872), [codingninja2](https://www.codingninjas.com/codestudio/problems/flip-bits_1063248)

* * * * *

### **Solution:**

-   convert the array 1 -> -1 and 0 -> 1

-   as we are losing 1 when we are fliping from 1 to 0 so we convert 1 to -1

-   and we are gaining when we are fliping from 0 to 1 so we convert 0 to 1

-   also count the number of ones

-   After converting the array as we have to find the maximum sum in the array the question becomes finding the maxiumum sum subarray so we will use kadanes algorithm

-   after running a loop we will get the maximum sum after converting the 0 to 1

-   then we will add the sum with the count of one and return

* * * * *

## **Que 3: Maximum subarray sum after K concatenation OR alias K-Concatenation Maximum Sum**

Links: [Leetcode](https://leetcode.com/problems/k-concatenation-maximum-sum/), [CodingNinjas](https://www.codingninjas.com/studio/guided-paths/data-structures-algorithms/content/118820/offering/1381873?leftPanelTab=0)

### **Approach:** [Link](https://www.pepcoding.com/resources/data-structures-and-algorithms-in-java-levelup/dynamic-programming/k_concatenation/topic)

* * * * *

## **Solution:**

-   If K is equal to 1, we can directly apply Kadane's Algorithm on the original array and get the maximum subarray sum.

-   If K is greater than 1, we need to consider two cases based on the sum of the original array:

-   If the sum of the original array is negative, the largest subarray sum will never include the entire concatenated array. Therefore, we only need to apply Kadane's Algorithm on the first two concatenated arrays to find the maximum subarray sum.

-   If the sum of the original array is positive, the largest subarray sum will include the entire concatenated array. We can calculate the maximum subarray sum of the first two concatenated arrays using Kadane's Algorithm and add (K-2) times the sum of the original array to it.