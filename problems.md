# Classic Problems: Pointers and Memory Access

---

## Problem 1: Two Sum in Sorted Array

**Description:**  
Given a sorted array `arr` and a target value `T`, return the indices of the two elements that sum up to `T`. Assume there is exactly one solution.

**Idea:**  
Use two pointers: one at the beginning (`left`) and one at the end (`right`) of the array. Move them inward depending on the sum.

**Hint:**  
If `arr[left] + arr[right] < T`, increment `left`. If greater, decrement `right`.

**Solution:**
```python
def two_sum(arr, T):
    left, right = 0, len(arr) - 1
    while left < right:
        s = arr[left] + arr[right]
        if s == T:
            return [left, right]
        elif s < T:
            left += 1
        else:
            right -= 1
```

---

## Problem 2: Detect Cycle in Linked List

**Description:**  
Given a linked list, determine whether it contains a cycle.

**Idea:**  
Use the fast and slow pointer method (Floyd’s Tortoise and Hare).

**Hint:**  
If the fast pointer ever equals the slow pointer, there is a cycle.

**Solution:**
```python
def has_cycle(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow == fast:
            return True
    return False
```

---

## Problem 3: Minimum Size Subarray Sum

**Description:**  
Given an array of positive integers `arr` and a positive integer `target`, return the minimal length of a contiguous subarray of which the sum is ≥ `target`. If there is no such subarray, return 0.

**Idea:**  
Use a sliding window with two pointers.

**Hint:**  
Expand the window by moving the end pointer, then shrink it from the start as long as the sum is ≥ `target`.

**Solution:**
```python
def min_subarray_len(target, arr):
    left = 0
    total = 0
    min_len = float('inf')
    for right in range(len(arr)):
        total += arr[right]
        while total >= target:
            min_len = min(min_len, right - left + 1)
            total -= arr[left]
            left += 1
    return 0 if min_len == float('inf') else min_len
```
