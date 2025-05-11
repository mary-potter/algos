# Concept Questions: Pointers and Memory Access

---

### Q1: What does the following C code print?

```c
int x = 10;
int *p = &x;
printf("%d", *p);
```

**A.** Memory address of x  
**B.** 10  
**C.** Compilation error  
**D.** Garbage value  

**Correct Answer:** B

---

### Q2: In the Two-Pointer Technique, when is it typically used to start pointers at both ends of the array?

**A.** To reverse an array  
**B.** To find a pivot  
**C.** To perform binary search  
**D.** To find two numbers that sum to a target in a sorted array  

**Correct Answer:** D

---

### Q3: What is the primary use of fast and slow pointers in linked lists?

**A.** Sorting a linked list  
**B.** Finding maximum value  
**C.** Detecting cycles  
**D.** Reversing the list  

**Correct Answer:** C

---

### Q4: Which of the following is true about memory access?

**A.** Random access is always faster than sequential  
**B.** Temporal locality prefers distant addresses  
**C.** Spatial locality favors accessing adjacent memory  
**D.** Cache misses happen only in linked lists  

**Correct Answer:** C

---

### Q5: What happens when you dereference a null pointer?

**A.** Returns 0  
**B.** Program crashes or undefined behavior  
**C.** Returns the memory address  
**D.** Compiles without issue and runs safely  

**Correct Answer:** B
