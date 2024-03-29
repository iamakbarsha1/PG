# Part - A (2M)

### 1. Diff. btw Linear Queue vs Circular Queue:

| S.no. | Linear Queue                                                                                                                                                                              | Circular Queue                                                                                            |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| 1.    | Arranges the data in a linear pattern.                                                                                                                                                    | Arranges the data in a circular order where the rear end is connected with the front end.                 |
| 2.    | The insertion and deletion operations are fixed i.e, done at the rear and front end respectively.                                                                                         | Insertion and deletion are not fixed and it can be done in any position.                                  |
| 3.    | Requires more memory space.                                                                                                                                                               | Requires less memory space.                                                                               |
| 4.    | In the case of a linear queue, the element added in the first position is going to be deleted in the first position. The order of operations performed on any element is fixed i.e, FIFO. | In the case of circular queue, the order of operations performed on an element may change.                |
| 6.    | In a linear queue, we can easily fetch out the peek value.                                                                                                                                | In a circular queue, we cannot fetch out the peek value easily.                                           |
| 7.    | **Application:-** <br>1. People standing for the bus. <br>2. Cars lined on a bridge.                                                                                                      | **Application-** <br>1. Computer-controlled traffic signal<br>2. In CPU scheduling and memory management. |
| 11.   | Not suitable for real-time systems where overflow can lead to data loss.                                                                                                                  | Suitable for real-time systems where continuous data insertion is required.                               |

### 2. Sorting Techniques:
- Selection Sort
- Bubble Sort
- Insertion Sort
- Merge Sort
- Quick Sort
- Heap Sort
--
- Counting Sort
- Radix Sort
- Bucket Sort
- Bingo Sort Algorithm
- ShellSort
- TimSort
- Comb Sort
- Pigeonhole Sort
- Cycle Sort
- Cocktail Sort
- Strand Sort
- Bitonic Sort
- Pancake sorting
- BogoSort or Permutation Sort
- Gnome Sort
- Sleep Sort – The King of Laziness
- Structure Sorting in C++
- Stooge Sort
- Tag Sort (To get both sorted and original)
- Tree Sort
- Odd-Even Sort / Brick Sort
- 3-way Merge Sort
### 3. State the Complexity Classes P and NP:

- Complexity Classes:
	- There exist some problems whose solutions are not yet found, the problems are divided into classes.
- Types of Complexity Classes
	- P Class
	- NP Class
	- CoNP Class
	- NP-hard
	- NP-complete
- P Class:
	- The P in the P class stands for Polynomial Time. 
	- It is the collection of decision problems(problems with a “yes” or “no” answer) that can be solved by a deterministic machine in polynomial time. 
- NP Class:
	- The NP in NP class stands for Non-deterministic Polynomial Time. 
	- It is the collection of decision problems that can be solved by a non-deterministic machine in polynomial time. 

### 4. Order traversal:
- Refers to traversing or visiting nodes in a tree data structure in a specific order. 
- There are different types of tree traversal techniques, each defining a specific order in which nodes are visited
- 3 types:
	- Inorder Traversal: 
		- In this traversal, nodes are visited in the order of left subtree, root, and then right subtree. 
		- It is commonly used for binary search trees (BST) to visit nodes in sorted order.
	- Preorder Traversal: 
		- Here, nodes are visited in the order of root, left subtree, and then right subtree. 
		- It is useful for creating a copy of the tree and evaluating expressions in prefix notation.
	- Postorder Traversal: 
		- In this traversal, nodes are visited in the order of left subtree, right subtree, and then root. 
		- It is commonly used for deleting nodes from a tree or evaluating expressions in postfix notation.

### 5. Convert the following infinite expression to prefix expression using stack (A*B+C/D):

**Input:** 
	A * B + C / D  
**Output:** 
	+ * A B/ C D

Infix Expression: 
	The expression of type a ‘operator’ b (a+b, where + is an operator) i.e., when the operator is between two operands.

Prefix Expression: 
	The expression of type ‘operator’ a b (+ab where + is an operator) i.e., when the operator is placed before the operands.

### 6. Structure of Singly Linked List:

A singly linked list is a linear data structure in which the elements are not stored in contiguous memory locations and each element is connected only to its next element using a pointer.

<img src="./Pasted image 20240329171607.png" alt="Pasted image 20240329171607.png" />

![[Pasted image 20240329171607.png]]

### 7. Merits of linked list over arrays in DSA:
- Dynamic Size
- Insertions and Deletions
- Memory Management
- Dynamic Data Structures
- Memory Allocation
- Flexibility

### 8. Linear search and its example?

- Linear search is a simple searching algorithm that sequentially checks each element in a list until a match is found or the end of the list is reached. It is also known as sequential search.

- Example:
	Consider an array of integers: [4, 2, 8, 5, 1, 9, 3, 6, 7]

### 9. Advantages of Recursive Function in DSA
- Simplified Code Structure
- Problem Decomposition
- Code Reusability
- Efficient Memory Usage
- Elegant Solutions
- Tail Recursion Optimization
- Facilitates Backtracking
- Flexibility

# Part - B

### 11. [Primitive and Non-primitive data-types in JavaScript](https://www.geeksforgeeks.org/primitive-and-non-primitive-data-types-in-javascript/)
- Every Variable has a data type that tells what kind of data is being stored in a variable. There are two types of data types in JavaScript.
	- Primitive data types 
	- Non-primitive data types 
- Primitive data types:
	- The predefined data types provided by JavaScript language are known as primitive data types. Primitive data types are also known as in-built data types.
	
#### Primitive Data Types:

1. Number: 
	1. Represents numeric values, both integers and floating-point numbers.
2. String: 
	1. Represents sequences of characters enclosed within single or double quotes.
3. Boolean: 
	1. Represents a logical value, either true or false.
4. Undefined: 
	1. Represents a variable that has been declared but not assigned a value.
5. Null: 
	1. Represents the intentional absence of any value.
6. Symbol (ES6): 
	1. Represents a unique and immutable data type, primarily used as object property keys.
```js
let sym = Symbol("Hello")
console.log(typeof(sym));
console.log(sym);

// symbol
// Symbol(Hello)
```
7. BigInt
	1. This data type can represent numbers greater than 253-1 which helps to perform operations on large numbers. 
```js
let bigNum = 123422222222222222222222222222222222222n
console.log(bigNum)

// 123422222222222222222222222222222222222n
```
#### Non-Primitive Data Types:

1. Object: 
	1. Represents a collection of key-value pairs, where each value can be of any data type, including other objects.
2. Array: 
	1. Represents a special type of object used to store multiple values in a single variable.
3. Function: 
	1. Represents a reusable block of code that performs a specific task.
```js
// Function declaration
function greet(name) {
    console.log("Hello, " + name + "!");
}

// Function call
greet("John");
```
5. Date: 
	1. Represents a specific point in time, including date and time information.
```js
// Current date and time
var currentDate = new Date();
console.log(currentDate);

// Specific date and time
var christmasDay = new Date(2024, 11, 25); // Months are zero-based (0 for January)
console.log(christmasDay);
```
6. RegExp: 
	1. Represents a regular expression used for pattern matching within strings.
```js
// Regular expression for matching email addresses
var emailRegex = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

// Test if a string matches the regex
var email = "example@email.com";
if (emailRegex.test(email)) {
    console.log("Valid email address.");
} else {
    console.log("Invalid email address.");
}
```
7. Map and Set (ES6): 
	1. Data structures for storing key-value pairs and unique values, respectively.
```js
// Map example: Storing key-value pairs
var userDetails = new Map();
userDetails.set("name", "John Doe");
userDetails.set("age", 30);
console.log(userDetails.get("name"));

// Set example: Storing unique values
var uniqueNumbers = new Set([1, 2, 3, 4, 5, 1, 2, 3]);
console.log(uniqueNumbers);
```

## Difference between Primitive vs Non-Primitive

| Primitive                                      | Non-Primitive                                          |
| ---------------------------------------------- | ------------------------------------------------------ |
| Primitive Data types are predefined.           | Non-Primitive data types are created by the programmer |
| Primitive Data types will have certain values. | Non-Primitive data types can be NULL.                  |
| Size depends on the type of data structure.    | Size is not fixed                                      |
| Examples are numbers and strings.              | Examples are Array and Linked List.                    |
| It can start with a lowercase.                 | It can start with uppercase.                           |
### 12. Types of Linked List

- A [linked list](https://www.geeksforgeeks.org/data-structures/linked-list/) is a linear data structure, in which the elements are not stored at contiguous memory locations. 
- The elements in a linked list are linked using [pointers](https://www.geeksforgeeks.org/pointers-in-c-and-c-set-1-introduction-arithmetic-and-array/). 
- In simple words, a linked list consists of nodes where each node contains a data field and a reference(link) to the next node in the list.


1. Singly Linked List:
    - Each node contains data and a reference to the next node.
    - Example: 1 -> 2 -> 3 -> null
2. Doubly Linked List:
    - Each node contains data, a reference to the next node, and a reference to the previous node.
    - Example: null <- 1 <-> 2 <-> 3 -> null
    - <img src="./Pasted image 20240329234843.png" alt="Pasted image 20240329234843.png" />
    - ![[Pasted image 20240329234843.png]]
1. Circular Linked List:
    - Last node's reference points back to the first node, forming a circular structure.
    - Example: 1 -> 2 -> 3 -> 1 (reference)
    - <img src="./Pasted image 20240330000206.png" alt="Pasted image 20240330000206.png" />
	- ![[Pasted image 20240330000206.png]]
2. Doubly Circular Linked List:
    - Combination of doubly linked list and circular linked list.
    - Example: null <- 1 <-> 2 <-> 3 -> null (reference to first and last nodes)
    - <img src="./Pasted image 20240330000303.png" alt="Pasted image 20240330000303.png" />
    - ![[Pasted image 20240330000303.png]]

#### 1.  Singly Linked List
- It is the simplest type of linked list in which every node contains some data and a pointer to the next node of the same data type. 
- The node contains a pointer to the next node means that the node stores the address of the next node in the sequence. 
- A single linked list allows the traversal of data only in one way

<img src="./Pasted image 20240329233458.png" alt="Pasted image 20240329233458.png" />

![[Pasted image 20240329233458.png]]

### 14. Implement Stack using Array: 
### **Step-by-Step Algorithm:**

1. **Initialization:**
    - Define the maximum size of the stack (`MAX_SIZE`).
    - Initialize the global variable `top` to -1.
    - Declare the stack array.
2. **Check if the Stack is Empty (`isEmpty`):**
    - Return `1` if `top` is -1, indicating an empty stack.
3. **Check if the Stack is Full (`isFull`):**
    - Return `1` if `top` is equal to `MAX_SIZE - 1`, indicating a full stack.
4. **Push Operation (`push`):**
    - Check if the stack is full.
    - Increment `top` and add the element to the stack.
    - Display a message indicating the element has been pushed.
5. **Pop Operation (`pop`):**
    - Check if the stack is empty.
    - Display and remove the element at the top of the stack.
    - Decrement `top`.
6. **Display Operation (`display`):**
    - Check if the stack is empty.
    - Display the elements of the stack from top to bottom.
7. **Main Function (`main`):**
    - Demonstrate the stack operations by pushing, displaying, and popping elements.

### Code:

```c
#include <stdio.h>
#include <stdlib.h>

// Define the maximum size of the stack
#define MAX_SIZE 5

// Initialize a global variable to represent the top of the stack
int top = -1;

// Declare the stack array
int stack[MAX_SIZE];

// Function to check if the stack is empty
int isEmpty() {
    return top == -1;
}

// Function to check if the stack is full
int isFull() {
    return top == MAX_SIZE - 1;
}

// Function to push an element onto the stack
void push(int item) {
    // Check if the stack is full before pushing
    if (isFull()) {
        printf("Stack Overflow! Cannot push element %d.\n", item);
        return;
    }

    // Increment the top and add the item to the stack
    top++;
    stack[top] = item;
    printf("Pushed %d onto the stack.\n", item);
}

// Function to pop an element from the stack
void pop() {
    // Check if the stack is empty before popping
    if (isEmpty()) {
        printf("Stack Underflow! Cannot pop from an empty stack.\n");
        return;
    }

    // Display and decrement the top to remove the item
    printf("Popped %d from the stack.\n", stack[top]);
    top--;
}

// Function to display the elements of the stack
void display() {
    // Check if the stack is empty before displaying
    if (isEmpty()) {
        printf("Stack is empty.\n");
        return;
    }

    // Display the elements from top to bottom
    printf("Stack elements: ");
    for (int i = top; i >= 0; i--) {
        printf("%d ", stack[i]);
    }
    printf("\n");
}

// Main function to demonstrate stack operations
int main() {
    // Pushing elements onto the stack
    push(10);
    push(20);
    push(30);
    push(40);
    push(50);

    // Displaying the current stack
    display();

    // Popping an element from the stack
    pop();

    // Displaying the updated stack
    display();

    return 0;
}
```

### Output:

```
Pushed 10 onto the stack.
Pushed 20 onto the stack.
Pushed 30 onto the stack.
Pushed 40 onto the stack.
Pushed 50 onto the stack.
Stack elements: 50 40 30 20 10 
Popped 50 from the stack.
Stack elements: 40 30 20 10 
```

### Explanation:

1. Pushed elements 10, 20, 30, 40, and 50 onto the stack.
2. Displayed the stack elements.
3. Popped an element from the stack (50 in this case).
4. Displayed the updated stack elements after the pop operation.
### 15. Quick sort algorithm:
```c
#include <stdio.h>

// Function to swap two elements
void swap(int* a, int* b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

// Function to partition the array and return the pivot index
int partition(int arr[], int low, int high) {
    int pivot = arr[high];
    int i = low - 1;

    for (int j = low; j < high; j++) {
        if (arr[j] <= pivot) {
            i++;
            swap(&arr[i], &arr[j]);
        }
    }
    swap(&arr[i + 1], &arr[high]);
    return i + 1;
}

// Recursive function to perform quick sort
void quick_sort(int arr[], int low, int high) {
    if (low < high) {
        int pivot_index = partition(arr, low, high);
        quick_sort(arr, low, pivot_index - 1);
        quick_sort(arr, pivot_index + 1, high);
    }
}

// Function to print an array
void print_array(int arr[], int size) {
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

// Driver code
int main() {
    int arr[] = {10, 7, 8, 9, 1, 5};
    int size = sizeof(arr) / sizeof(arr[0]);
    
    printf("Original array: \n");
    print_array(arr, size);
    
    quick_sort(arr, 0, size - 1);
    
    printf("Sorted array: \n");
    print_array(arr, size);
    
    return 0;
}
```

#### Algorithm:

1. Choose a pivot element from the array. (usually the last element)
2. Partition the array such that all elements smaller than the pivot are placed to its left, and all elements greater than the pivot are placed to its right.
3. Recursively apply the above steps to the sub-arrays on the left and right of the pivot until the entire array is sorted.
