**Selection Sort**

**Algorithm:**
1. Input: An array of elements.
2. Output: Sorted array in ascending order.
3. Procedure:
	- Start with the first element as the minimum.
	- Traverse the unsorted part of the array to find the minimum element.
	- Swap the minimum element with the first element.
	- Move the boundary between the sorted and unsorted parts one element to the right.
	- Repeat steps 1-5 bullets until the entire array is sorted.

**Code:**

```c
#include <stdio.h>

// Function to swap two elements
void swap(int *xp, int *yp) {
    int temp = *xp;
    *xp = *yp;
    *yp = temp;
}

// Function to perform Selection Sort
void selectionSort(int arr[], int n) {
    for (int i = 0; i < n-1; i++) {
        // Assume the current index is the minimum
        int min_idx = i;

        // Traverse the unsorted part to find the minimum element
        for (int j = i+1; j < n; j++)
            if (arr[j] < arr[min_idx])
                min_idx = j;

        // Swap the found minimum element with the first element
        swap(&arr[min_idx], &arr[i]);
    }
}

// Function to print an array
void printArray(int arr[], int size) {
    for (int i = 0; i < size; i++)
        printf("%d ", arr[i]);
    printf("\n");
}

int main() {
    int arr[] = {64, 25, 12, 22, 11};
    int n = sizeof(arr)/sizeof(arr[0]);

    printf("Original array: \n");
    printArray(arr, n);

    // Perform Selection Sort
    selectionSort(arr, n);

    printf("Sorted array: \n");
    printArray(arr, n);

    return 0;
}
```

### Output:

The provided C program performs the Selection Sort algorithm on the array `{64, 25, 12, 22, 11}`. Let's go through the output step by step:


**Original array:**
```
64 25 12 22 11
```

**After the 1st pass:**
- Minimum element in the unsorted part is `11`, swap it with the first element.
```
11 25 12 22 64
```

**After the 2nd pass:**
- Minimum element in the unsorted part is `12`, swap it with the second element.
```
11 12 25 22 64
```

**After the 3rd pass:**
- Minimum element in the unsorted part is `22`, swap it with the third element.
```
11 12 22 25 64
```

**After the 4th pass:**
- Minimum element in the unsorted part is `25`, swap it with the fourth element.
```
11 12 22 25 64
```


**Sorted array:**
```
11 12 22 25 64
```

So, the final sorted array is 
```
{11, 12, 22, 25, 64}
```
