# Concept Snippets: Pointers and Memory Access

---

## 1. What is a Pointer?

A pointer is a variable that stores the memory address of another variable. In languages like C/C++, you use `*` to declare and dereference pointers.

```c
int a = 5;
int *p = &a;
```

---

## 2. Pointer Arithmetic

You can perform arithmetic on pointers to traverse memory. Useful when working with arrays.

```c
int arr[3] = {1, 2, 3};
int *p = arr;
*(p + 1); // Accesses arr[1]
```

---

## 3. Null and Dangling Pointers

A null pointer is one that doesn't point to any memory. A dangling pointer points to memory that has been freed.

```c
int *ptr = NULL;
```

---

## 4. The Two-Pointer Technique

Use two pointers to solve problems like finding pairs, checking palindromes, or implementing sliding windows.

```python
left, right = 0, len(arr) - 1
while left < right:
    # process
    left += 1
    right -= 1
```

---

## 5. Fast and Slow Pointers

Used in cycle detection and finding midpoints in linked lists.

```python
slow = fast = head
while fast and fast.next:
    slow = slow.next
    fast = fast.next.next
```

---

## 6. Sliding Window Pattern

Maintain a dynamic range with two pointers, optimizing for conditions like sum or length.

```python
start = 0
for end in range(len(arr)):
    while window_not_valid():
        start += 1
```

---

## 7. Memory Access Patterns

Sequential access is cache-friendly. Random access can lead to cache misses.

```python
# Better for cache
for i in range(len(arr)):
    process(arr[i])
```

---

## 8. Python List References

Even without raw pointers, Python passes references. Be cautious of mutability.

```python
a = [1, 2]
b = a
b.append(3)  # a is now [1, 2, 3]
```
