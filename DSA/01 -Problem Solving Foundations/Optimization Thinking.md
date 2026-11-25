
---

# 📋 `19 - Optimization Thinking`

```markdown
# 19 - Optimization Thinking

> **Optimization means reducing unnecessary computational work or memory usage while preserving correctness.**

---

# 1. The Wrong Mindset

Do not think:

> "I need a clever algorithm."

Think:

> **"Where is my current solution wasting work?"**

---

# 2. Optimization Cycle

```text
Correct Solution
      ↓
Analyze Complexity
      ↓
Find Bottleneck
      ↓
Understand Repeated Work
      ↓
Find Better Representation / Pattern
      ↓
Optimize
      ↓
Verify Correctness

```
# 3. Main Optimization Questions

Ask:

### 1. Am I repeating work?

If yes, consider:

```
HashMap
HashSet
Memoization
Prefix Sum
```

---

### 2. Am I checking unnecessary pairs?

Consider:

```
Two Pointers
Sorting
Hashing
```

---

### 3. Am I repeatedly processing a range?

Consider:

```
Prefix Sum
Sliding Window
```

---

### 4. Is the data sorted?

Consider:

```
Binary Search
Two Pointers
```

---

### 5. Do I need the minimum/maximum repeatedly?

Consider:

```
Heap / PriorityQueue
```

---

### 6. Am I exploring the same states repeatedly?

Consider:

```
Dynamic Programming
Memoization
```

---

### 7. Is the problem hierarchical?

Consider:

```
Tree / DFS / BFS
```

---

### 8. Is it about connectivity?

Consider:

```
Graph
Union-Find
DFS / BFS
```

---

# 4. Example — Duplicate Detection

### Brute Force

```
Compare every pair
```

Complexity:

```
O(n²)
```

### Observation

We repeatedly ask:

> "Have I already seen this value?"

### Optimization

Use:

```
HashSet
```

Complexity:

```
Time → O(n) average
Space → O(n)
```

---

# 5. Example — Range Sum

Suppose we repeatedly calculate:

```
sum of arr[l...r]
```

Brute force:

```
Traverse every element in the range
```

Repeated queries can become expensive.

### Observation

Prefix information can be reused.

Use:

```
Prefix Sum
```

Then range sum can be calculated in constant time after preprocessing:

```
O(1)
```

while preprocessing takes:

```
O(n)
```

---

# 6. Optimization Is Often a Trade-off

Improving time may require more memory.

Example:

```
Brute Force
Time  → O(n²)
Space → O(1)
```

Hashing:

```
Time  → O(n)
Space → O(n)
```

We traded:

```
Memory
   ↓
for
   ↓
Speed
```

---

# 7. Common Optimization Patterns

|Bottleneck|Possible Technique|
|---|---|
|Repeated lookup|HashMap / HashSet|
|Repeated range sum|Prefix Sum|
|Pair searching|Two Pointers / Hashing|
|Repeated subarray processing|Sliding Window|
|Sorted search|Binary Search|
|Repeated min/max|Heap|
|Repeated states|DP / Memoization|
|Hierarchical traversal|DFS / BFS|
|Connectivity|Union-Find|

---

# 8. Optimization Does Not Mean "Lowest Big O" Always

Example:

```
O(n)
```

is asymptotically better than:

```
O(n²)
```

but practical performance also depends on:

- Constants
- Memory usage
- Cache behavior
- Input size
- Implementation
- Constraints

Therefore:

> Choose an algorithm that is sufficiently efficient for the constraints and appropriate for the problem.

---

# 9. Optimization Checklist

Before finalizing a solution:

```
□ Is it correct?
□ What is the time complexity?
□ What is the space complexity?
□ Is there repeated work?
□ Can I reduce unnecessary loops?
□ Can I use a better data structure?
□ Can I preprocess information?
□ Can I exploit sorting?
□ Can I reduce the search space?
□ Do the constraints allow my solution?
□ Are edge cases handled?
```

---

# 10. Most Important Optimization Principle

> **Don't optimize blindly. First identify the bottleneck.**

```
Slow Solution
     ↓
Why is it slow?
     ↓
Repeated work?
     ↓
Can information be stored/reused?
     ↓
Better data structure / pattern
     ↓
Faster Solution
```

---

# 11. Golden Rule

> **Optimization is usually about avoiding work, not doing the same work faster.**