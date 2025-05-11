# Concept Questions: Pointers and Memory Access

---

### Q1: What is a pointer and how is it used in programming?

**Answer:**  
A pointer is a variable that stores the memory address of another variable. It is used to directly access and manipulate memory, allowing efficient array traversal, dynamic memory allocation, and data structure implementation.

---

### Q2: What are the main differences between stack and heap memory?

**Answer:**  
Stack memory is automatically managed and used for static memory allocation (e.g., local variables), while heap memory is dynamically managed and used for objects whose lifetime is controlled manually. Stack is faster but limited in size; heap is larger but slower.

---

### Q3: Explain the two-pointer technique with an example.

**Answer:**  
The two-pointer technique involves using two indices to traverse a data structure, often to reduce time complexity. For example, to find two numbers in a sorted array that sum to a target, one pointer starts from the beginning, another from the end, and they move inward based on the sum.

---

### Q4: What is pointer arithmetic and when is it useful?

**Answer:**  
Pointer arithmetic involves adding or subtracting integers to move a pointer across contiguous memory blocks, such as arrays. It's useful for iterating through memory efficiently without relying on indices.

---

### Q5: Why is understanding memory access patterns important for performance?

**Answer:**  
Efficient memory access patterns, such as sequential access, utilize CPU caching better and lead to faster execution. Poor access patterns can cause cache misses, increasing latency and degrading performance.
