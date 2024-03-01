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