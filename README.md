#include <stdio.h>

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    int n = sizeof(arr) / sizeof(arr[0]);

    int last = arr[n - 1];

    // Shift elements to the right
    for (int i = n - 1; i > 0; i--) {
        arr[i] = arr[i - 1];
    }

    // Put last element at first position
    arr[0] = last;

    printf("Array after rotation: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
OUTPUT
Array after rotation: 5 1 2 3 4
PYTHON
arr = [1, 2, 3, 4, 5]

# Store last element
last = arr[-1]

# Shift elements to the right
for i in range(len(arr) - 1, 0, -1):
    arr[i] = arr[i - 1]

# Put last element at first position
arr[0] = last

print("Array after rotation:", arr)
Array after rotation: [5, 1, 2, 3, 4]
# Rotate-array-by-one
