
---

> The goal is not to recognize every problem. The goal is to develop a process for solving unfamiliar problems.

---

# 1. First Rule

When seeing a new problem:

> **Do not immediately search for a pattern. Understand the problem first.**

---

# 2. Step 1 — Understand

Ask:

```text
What is the input?
What is the output?
What exactly must be found?
What operations are allowed?

```
Rewrite the problem in your own words.

---

# 3. Step 2 — Study Constraints

Look for:

```
n ≤ ?
Value range?
Number of test cases?
Sorted?
Duplicates?
Negative values?
```

Constraints strongly influence the possible complexity.

---

# 4. Step 3 — Create Examples

Use a small example.

Then test:

```
Normal case
Small case
Edge case
```

---

# 5. Step 4 — Brute Force

Ask:

> What is the simplest correct solution?

Do not worry about optimization yet.

---

# 6. Step 5 — Analyze

Calculate:

```
Time Complexity
Space Complexity
```

Then ask:

> Will this pass the constraints?

---

# 7. Step 6 — Find the Bottleneck

Look for:

- Repeated searching
- Repeated calculation
- Nested loops
- Repeated sorting
- Unnecessary traversal
- Duplicate work

---

# 8. Step 7 — Look for Patterns

Possible patterns:

```
HashMap / HashSet
Two Pointers
Sliding Window
Prefix Sum
Binary Search
Stack
Heap
BFS
DFS
Greedy
Dynamic Programming
```

Do not force a pattern.

---

# 9. Step 8 — Optimize

```
Brute Force
    ↓
Bottleneck
    ↓
Observation
    ↓
Data Structure / Pattern
    ↓
Optimized Algorithm
```

---

# 10. Step 9 — Prove With Examples

Test:

```
Normal
Edge
Boundary
Worst-case
```

---

# 11. Step 10 — Explain

Be able to state:

```
Approach
Why it works
Time complexity
Space complexity
```

---

# 12. When Stuck

Do not immediately look at the solution.

Try:

```
1. Restate problem
2. Solve smaller input
3. Write brute force
4. Find repeated work
5. Draw the data
6. Try another data structure
7. Check constraints
8. Try a related known pattern
```

---

# 13. Example Thinking

Problem:

> Find two numbers whose sum equals target.

Start:

```
Brute Force
→ Check every pair
→ O(n²)
```

Ask:

> Why am I repeatedly searching for the complement?

Use:

```
HashMap / HashSet
```

Optimized:

```
O(n) average
```

The important part is not memorizing Two Sum.

It is recognizing:

```
Repeated lookup
      ↓
Can I store previous information?
      ↓
Hashing
```

---

# 14. Final Problem-Solving Framework

```
UNDERSTAND
    ↓
EXAMPLES
    ↓
CONSTRAINTS
    ↓
BRUTE FORCE
    ↓
COMPLEXITY
    ↓
BOTTLENECK
    ↓
OBSERVATION
    ↓
PATTERN
    ↓
OPTIMIZE
    ↓
EDGE CASES
    ↓
TEST
    ↓
EXPLAIN
```

> **This process is more valuable than memorizing hundreds of solutions.**