# Static and Dynamic Arrays

## Overview
An **array** is a data structure used to store a collection of elements of the same type. Arrays provide efficient access to elements using an index and are widely used in programming. Arrays can be classified into **static** and **dynamic** arrays based on how their memory is allocated and managed.

---

## 1. Static Arrays
A **static array** is an array with a fixed size that is determined at the time of its creation. The size of a static array cannot be changed during runtime.

### Characteristics
- **Fixed Size:** The size of the array is predefined and cannot be modified.
- **Contiguous Memory Allocation:** The memory is allocated in a continuous block.
- **Fast Access:** Elements can be accessed in O(1) time using indexing.
- **Memory Efficiency:** There is no extra memory overhead since the size is predetermined.

### Example (C++)
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {1, 2, 3, 4, 5}; // Static array of size 5
    cout << arr[2]; // Accessing the third element (index 2)
    return 0;
}
```

### Pros and Cons
**Pros:**
- Faster access due to contiguous memory allocation.
- Efficient in terms of memory if the size is known beforehand.

**Cons:**
- Cannot be resized once created.
- Wastes memory if allocated size is larger than needed.

---

## 2. Dynamic Arrays
A **dynamic array** is an array that can change its size during runtime. It allows elements to be added or removed as needed.

### Characteristics
- **Resizable:** Can grow or shrink in size dynamically.
- **Heap Allocation:** Memory is allocated on the heap instead of the stack.
- **Reallocation Overhead:** If the array grows beyond its initial capacity, a new larger array is created, and elements are copied over.
- **Efficient Access:** Similar to static arrays, accessing elements is O(1) time complexity.

### Example (C++ using `vector`)
```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> arr = {1, 2, 3}; // Dynamic array using vector
    arr.push_back(4); // Add an element at runtime
    cout << arr[3]; // Accessing the fourth element
    return 0;
}
```

### Pros and Cons
**Pros:**
- Can dynamically resize as needed.
- No memory wastage as the size adjusts according to usage.

**Cons:**
- Slower resizing due to memory reallocation and copying.
- More memory overhead for resizing and managing metadata.

---

## Differences Between Static and Dynamic Arrays
| Feature            | Static Array          | Dynamic Array         |
|--------------------|----------------------|-----------------------|
| Size              | Fixed                 | Flexible (resizable)  |
| Memory Allocation | Stack                 | Heap                  |
| Performance       | Faster (no resizing)  | Slower due to resizing|
| Memory Efficiency | No overhead           | Some overhead for resizing |
| Usability        | Simple and efficient  | More flexible         |

---

## Conclusion
- **Use static arrays** when the size is known and fixed for better performance and memory efficiency.
- **Use dynamic arrays** when the size is unknown or changes frequently, even though they have more overhead.

Both types have their use cases, and choosing the right one depends on the problem's requirements.
