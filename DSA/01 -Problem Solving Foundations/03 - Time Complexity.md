

> **Time Complexity:** A measure of how the computational work of an algorithm grows as the input size increases.

---

# 1. Why Do We Need Time Complexity?

Two algorithms can solve the same problem but perform very different amounts of work.

Example:

```text
Algorithm A → 100 operations
Algorithm B → 1,000,000 operations
```
For a small input, both may appear fast.

For a large input, the difference can become huge.

We therefore need to understand:

> **How does the algorithm scale when the input becomes larger?**

---

# 2. Why Not Just Measure Execution Time?

Actual runtime depends on:

- CPU
- RAM
- JVM/compiler
- Operating system
- Programming language
- Implementation details
- Background processes

So instead of focusing only on seconds, DSA focuses on the **growth of computational work**.

---

# 3. Input Size

Input size is usually represented by `n`.

Examples:

```
Array        → n = number of elements
String       → n = length of string
Matrix       → n may represent dimension
Graph        → V = vertices, E = edges
```

Example:

```
arr = [10, 20, 30, 40, 50]

n = 5
```

---

# 4. The Core Idea

Always ask:

> **As n increases, how does the amount of work increase?**

Example:

```
n = 10      → 10 operations
n = 100     → 100 operations
n = 1000    → 1000 operations
```

Work grows with `n`.

Therefore:

```
O(n)
```

---

# 5. Basic Operation

Operations such as these are generally treated as constant-time operations:

```
int x = 10;
x++;
int sum = a + b;
```

Their number of operations does not depend on `n`.

Therefore:

```
O(1)
```

> In complexity analysis, we normally treat primitive operations as constant-time under the standard RAM-style model. Real hardware costs can be more complicated.

---

# 6. O(1) — Constant Time

The amount of work does not grow with `n`.

Example:

```
int x = arr[0];
```

Typical complexity:

```
O(1)
```

Mental model:

```
n increases
   ↓
work remains approximately constant
```

Examples:

- Accessing an array element by index
- Arithmetic operation
- Assignment
- Comparing two values

---

# 7. O(n) — Linear Time

The amount of work grows proportionally with `n`.

Example:

```
for (int i = 0; i < n; i++) {
    System.out.println(arr[i]);
}
```

The loop executes approximately `n` times.

Therefore:

```
O(n)
```

Mental model:

```
n doubles
   ↓
work ≈ 2×
```

Common examples:

- Linear search
- Finding maximum in an unsorted array
- Traversing an array
- Counting elements

---

# 8. Example — Find Maximum

```
int max = arr[0];

for (int i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
        max = arr[i];
    }
}
```

For `n` elements:

```
Comparisons ≈ n - 1
```

Therefore:

```
Time → O(n)
```

Extra variables used:

```
Space → O(1)
```

---

# 9. Why Finding Maximum Is Ω(n)

Consider:

```
[5, 8, 2, 10, 4]
```

If we do not inspect the last element, it could be:

```
1000
```

Therefore, in the worst case we need to examine all elements.

So:

```
Upper bound → O(n)
Lower bound → Ω(n)
Tight bound  → Θ(n)
```

This means the standard linear solution is asymptotically optimal.

---

# 10. O(n²) — Quadratic Time

Example:

```
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        // constant work
    }
}
```

Outer loop:

```
n
```

Inner loop for each outer iteration:

```
n
```

Total:

```
n × n = n²
```

Therefore:

```
O(n²)
```

Common examples:

- Comparing every pair
- Bubble Sort
- Selection Sort
- Simple brute-force duplicate checking

---

# 11. O(n³) — Cubic Time

```
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        for (int k = 0; k < n; k++) {
        }
    }
}
```

Total:

```
n × n × n
= n³
```

Therefore:

```
O(n³)
```

---

# 12. IMPORTANT — Nested Loops ≠ Automatically O(n²)

Consider:

```
for (int i = 0; i < n; i++) {
    for (int j = 0; j < 10; j++) {
    }
}
```

Total work:

```
n × 10
= 10n
```

Drop the constant:

```
O(n)
```

### Important Rule

> **Do not count loops. Count total work.**

---

# 13. Sequential Loops

```
for (int i = 0; i < n; i++) {
}

for (int j = 0; j < n; j++) {
}
```

Complexity:

```
O(n) + O(n)
= O(2n)
= O(n)
```

### Rule

> **Sequential operations are added.**

---

# 14. Nested Operations

```
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
    }
}
```

Complexity:

```
O(n × n)
= O(n²)
```

### Rule

> **Independent nested work is often multiplied, but always inspect the loop bounds.**

---

# 15. O(log n) — Logarithmic Time

Consider:

```
for (int i = 1; i < n; i *= 2) {
}
```

Values:

```
1 → 2 → 4 → 8 → 16 → 32 → ...
```

After `k` iterations:

```
2^k ≈ n
```

Therefore:

```
k ≈ log₂(n)
```

So:

```
O(log n)
```

---

# 16. Recognizing Logarithmic Loops

These patterns often indicate logarithmic complexity:

```
i *= 2
i *= 3
i *= k
```

or:

```
i /= 2
i /= 3
i /= k
```

provided the loop progresses toward the termination condition.

### Mental model

```
Multiply / Divide
       ↓
Search space changes exponentially
       ↓
Number of iterations grows logarithmically
       ↓
O(log n)
```

---

# 17. Why O(log n) Is Powerful

For:

```
n = 1,000,000
```

approximately:

```
log₂(1,000,000) ≈ 20
```

So an O(log n) algorithm may need only around 20 iterations.

Compare:

```
O(n)     → ≈ 1,000,000
O(log n) → ≈ 20
```

This is the basic reason Binary Search is so efficient.

---

# 18. O(n log n)

A very common complexity in DSA.

Examples:

- Merge Sort
- Heap Sort
- Many divide-and-conquer algorithms

Mental model:

```
n work
  ×
log n levels
  =
n log n
```

---

# 19. Variable Loop Bounds

Do not blindly multiply loop limits.

Example:

```
for (int i = 0; i < n; i++) {
    for (int j = 0; j < i; j++) {
    }
}
```

Total work:

```
0 + 1 + 2 + 3 + ... + (n - 1)
```

Formula:

```
n(n - 1) / 2
```

Dominant term:

```
n²
```

Therefore:

```
O(n²)
```

---

# 20. Another Important Example

```
for (int i = 0; i < n; i++) {
    for (int j = 0; j < i * i; j++) {
    }
}
```

For each `i`, inner loop runs approximately:

```
i²
```

Total:

```
0² + 1² + 2² + ... + (n - 1)²
```

The sum grows as:

```
Θ(n³)
```

Therefore:

```
O(n³)
```

---

# 21. Nested Logarithmic Loops

```
for (int i = 1; i < n; i *= 2) {
    for (int j = 1; j < n; j *= 2) {
    }
}
```

Outer:

```
O(log n)
```

Inner:

```
O(log n)
```

Total:

```
O(log n × log n)
```

Therefore:

```
O(log² n)
```

---

# 22. Drop Constants

Suppose:

```
T(n) = 5n
```

Then:

```
O(5n) = O(n)
```

Similarly:

```
O(100n) = O(n)
O(10n²) = O(n²)
```

> Constants are ignored when describing asymptotic growth.

---

# 23. Keep the Dominant Term

Suppose:

```
T(n) = n² + n + 100
```

For large `n`:

```
n² dominates n and 100
```

Therefore:

```
O(n²)
```

Another example:

```
n³ + n² + n
```

becomes:

```
O(n³)
```

### Rule

> **Keep the fastest-growing term.**

---

# 24. Complexity Hierarchy

From slower growth to faster growth:

```
O(1)
   ↓
O(log n)
   ↓
O(n)
   ↓
O(n log n)
   ↓
O(n²)
   ↓
O(n³)
   ↓
O(2ⁿ)
   ↓
O(n!)
```

For large input:

> Lower growth rate generally means better scalability.

---

# 25. Doubling Input Size

This is extremely important for intuition.

### O(n)

```
n → 2n
```

Work:

```
≈ 2×
```

### O(n²)

```
n → 2n

(2n)² = 4n²
```

Work:

```
≈ 4×
```

### O(n³)

```
(2n)³ = 8n³
```

Work:

```
≈ 8×
```

### O(log n)

```
log(2n) = log n + log 2
```

Only a small increase.

---

# 26. Best, Average and Worst Case

These describe **different input situations**.

Example: Linear Search

```
for (int i = 0; i < n; i++) {
    if (arr[i] == target) {
        return i;
    }
}
```

### Best Case

Target is first:

```
O(1)
```

### Worst Case

Target is last or absent:

```
O(n)
```

### Average Case

Depends on assumptions about the distribution of inputs.

Often analyzed as:

```
O(n)
```

---

# 27. Big-O Does NOT Mean "Worst Case"

Common misconception:

> Big-O = Worst Case

Technically incorrect.

Big-O describes an **asymptotic upper bound**.

Best, average, and worst-case behavior can each be described using asymptotic notation.

Keep these concepts separate:

```
Best / Average / Worst
        ↓
Input scenario

O / Ω / Θ
        ↓
Asymptotic bound
```

---

# 28. O, Ω and Θ

For now remember:

```
O(f(n))  → Upper bound
Ω(f(n))  → Lower bound
Θ(f(n))  → Tight bound
```

Example: Finding maximum in an unsorted array:

```
O(n)
Ω(n)
Θ(n)
```

Detailed definitions are covered in the dedicated Big-O, Big-Theta and Big-Omega notes.

---

# 29. Time Complexity Is Not Exact Runtime

If an algorithm is:

```
O(n)
```

it does NOT mean:

```
n elements = n seconds
```

It means:

> The computational work grows approximately linearly with the input size.

Two algorithms can both be O(n) but have different actual runtimes because of constants and implementation details.

---

# 30. Constraints

Before solving a coding problem, always check:

> **What is the maximum possible value of n?**

Example:

```
n ≤ 20
```

Brute force or even exponential approaches may sometimes be possible.

```
n ≤ 1,000
```

O(n²) may often be possible.

```
n ≤ 100,000
```

O(n²) is usually suspicious.

```
n ≤ 1,000,000
```

Usually look for O(n), O(n log n), or sometimes O(log n), depending on the problem.

> These are heuristics, not strict laws. Always consider the actual problem and time limit.

---

# 31. Time Complexity of Common Algorithms

|Algorithm|Typical Time Complexity|
|---|---|
|Array index access|O(1)|
|Linear Search|O(n)|
|Binary Search|O(log n)|
|Merge Sort|O(n log n)|
|Heap Sort|O(n log n)|
|Bubble Sort|O(n²)|
|Selection Sort|O(n²)|
|Insertion Sort|O(n²) worst case|

> Always check best, average, and worst-case behavior when the distinction matters.

---

# 32. How to Calculate Time Complexity

When given code, follow this process:

### Step 1 — Identify input size

```
What does n represent?
```

### Step 2 — Find the basic repeated operation

```
Comparison?
Assignment?
Array access?
Function call?
```

### Step 3 — Count how many times it runs

### Step 4 — Analyze every loop

Ask:

```
Does it increase by 1?
Does it multiply?
Does it divide?
Does it depend on another loop?
```

### Step 5 — Analyze recursion if present

### Step 6 — Combine the work

### Step 7 — Remove constants

### Step 8 — Keep the dominant term

### Final question

> **How many times does the important operation execute as a function of n?**

---

# 33. Example of Complete Analysis

```
for (int i = 0; i < n; i++) {
}

for (int j = 0; j < n * n; j++) {
}
```

First loop:

```
O(n)
```

Second loop:

```
O(n²)
```

Total:

```
O(n + n²)
```

Dominant term:

```
O(n²)
```

Final answer:

```
Time Complexity = O(n²)
```

---

---

# 34. Most Important Rules to Memorize

> **1. Sequential work → Add**

```
O(n) + O(n) = O(n)
```

> **2. Nested work → Usually multiply**

```
O(n) × O(n) = O(n²)
```

> **3. Constant bounds disappear**

```
O(10n) = O(n)
```

> **4. Keep the dominant term**

```
O(n² + n) = O(n²)
```

> **5. Multiplication/division of loop variable → Often logarithmic**

```
i *= 2 → O(log n)
```

> **6. Always inspect the actual loop bounds.**

> **7. Always check the constraints.**

> **8. Analyze Time and Space separately.**

---

# 35. Quick Complexity Table

|Pattern|Complexity|
|---|---|
|One statement|O(1)|
|One loop to n|O(n)|
|Two sequential loops to n|O(n)|
|Two nested loops to n|O(n²)|
|Three nested loops to n|O(n³)|
|Loop with `i *= 2`|O(log n)|
|Loop with `i /= 2`|O(log n)|
|n work at log n levels|O(n log n)|
|Two nested log loops|O(log² n)|

---

# 36. Quick Revision — Growth

```
O(1)        Constant
O(log n)    Logarithmic
O(n)        Linear
O(n log n)  Linearithmic
O(n²)       Quadratic
O(n³)       Cubic
O(2ⁿ)       Exponential
O(n!)       Factorial
```

---

# 37. Interview Questions

### Basic

- What is Time Complexity?
- Why do we need it?
- What does `n` represent?
- What is O(1)?
- What is O(n)?
- What is O(log n)?
- What is O(n²)?

### Understanding

- Why is array index access O(1)?
- Why is linear search O(n)?
- Why is binary search O(log n)?
- Why does `i *= 2` produce O(log n)?
- Why is `n × 10 = O(n)`?
- Why is `n + n² = O(n²)`?
- Why don't nested loops always mean O(n²)?

### Interview-Level

- Does Big-O always mean worst case?
- What is the difference between O, Ω and Θ?
- Why is finding maximum in an unsorted array Ω(n)?
- Can two O(n) algorithms have different actual runtimes?
- Why are constraints important?
- How do you analyze a loop whose inner bound depends on the outer loop?