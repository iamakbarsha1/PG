Provide the code with comments, step-by-step algorithm for the C program for Quick sort.

### Algorithm:

1. **Partitioning (`partition`):**
    - Choose the rightmost element (`arr[high]`) as the pivot.
    - Initialize the index `i` to `low - 1`.
    - Traverse the array and rearrange elements based on the pivot.
    - Swap elements smaller than the pivot with `arr[i]` and increment `i`.
    - Swap `arr[i + 1]` and `arr[high]` to place the pivot in its correct position.
    - Return the pivot index.
2. **Quick Sort (`quickSort`):**
    - If `low` is less than `high`, find the pivot index using the `partition` function.
    - Recursively call `quickSort` on the sub-arrays on the left and right of the pivot.
3. **Print Array (`printArray`):**
    - Display the elements of the array.
4. **Main Function (`main`):**
    - Initialize an array and its size.
    - Print the original array.
    - Call `quickSort` to sort the array.
    - Print the sorted array.

### Code:

```c
#include <stdio.h>

// Function to partition the array and return the pivot index
int partition(int arr[], int low, int high) {
    // Choose the rightmost element as the pivot
    int pivot = arr[high];
    int i = low - 1;

    // Traverse the array and rearrange elements based on the pivot
    for (int j = low; j < high; j++) {
        if (arr[j] < pivot) {
            i++;
            // Swap arr[i] and arr[j]
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }

    // Swap arr[i + 1] and arr[high] to place the pivot in its correct position
    int temp = arr[i + 1];
    arr[i + 1] = arr[high];
    arr[high] = temp;

    // Return the pivot index
    return i + 1;
}

// Function to perform quick sort
void quickSort(int arr[], int low, int high) {
    if (low < high) {
        // Find the pivot index such that elements on the left are smaller and on the right are greater
        int pivotIndex = partition(arr, low, high);

        // Recursively sort the sub-arrays on the left and right of the pivot
        quickSort(arr, low, pivotIndex - 1);
        quickSort(arr, pivotIndex + 1, high);
    }
}

// Function to print an array
void printArray(int arr[], int size) {
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

// Main function to test the Quick Sort implementation
int main() {
    int arr[] = {64, 25, 12, 22, 11};
    int size = sizeof(arr) / sizeof(arr[0]);

    printf("Original array: ");
    printArray(arr, size);

    quickSort(arr, 0, size - 1);

    printf("Sorted array: ");
    printArray(arr, size);

    return 0;
}

```