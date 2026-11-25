
---



```markdown

> A good interview solution is not just correct code. You must communicate your reasoning clearly.

---

# 1. Recommended Structure

Use:

```text
1. Understand the problem
2. Brute force
3. Limitation
4. Observation
5. Optimized approach
6. Correctness
7. Complexity
8. Edge cases
9. Code
```
# 2. Start With the Problem

Say:

> "Let me first restate the problem to make sure I understand it correctly."

Then explain:

- Input
- Output
- Goal

---

# 3. Explain Brute Force

Say:

> "A straightforward approach would be..."

Explain:

```
Approach
↓
Complexity
```

---

# 4. Explain the Limitation

Do not simply say:

> "This is slow."

Say:

> "The problem is that we repeatedly perform the same search/work, resulting in O(n²) time."

---

# 5. Introduce the Optimization

Explain the observation:

> "Instead of repeatedly searching, I can store previously seen information in a HashMap."

This makes the transition logical.

---

# 6. Explain Why It Works

State the invariant or reasoning.

Example:

> "For each element, I check whether the required complement has already been seen."

---

# 7. Complexity

Always state both:

```
Time Complexity → O(?)
Space Complexity → O(?)
```

And explain why.

---

# 8. Edge Cases

Mention relevant cases:

- Empty input
- One element
- Duplicates
- Negative values
- Boundary values

Do not list irrelevant cases mechanically.

---

# 9. Code

Write clear code.

Avoid unnecessary cleverness.

---

# 10. Example Interview Flow

```
Problem
  ↓
Brute Force
  ↓
O(n²)
  ↓
Why too slow?
  ↓
Repeated lookup
  ↓
HashMap
  ↓
O(n) average
  ↓
Edge Cases
  ↓
Code
```

---

# 11. Strong Explanation Template

> "The straightforward approach is ____, which takes O(**) time. The bottleneck is ____. We can avoid this repeated work by using ____. For each element, I ____. This reduces the time complexity to O(**) with O(__) extra space. I would also handle ____ edge cases."

---

# 12. Common Interview Mistakes

Avoid:

- Jumping directly into code
- Saying "I know this problem"
- Giving memorized solutions
- Not discussing complexity
- Ignoring constraints
- Writing code before explaining the approach
- Being unable to explain your own code

---

# 13. If Interviewer Asks "Why?"

Be ready to explain:

```
Why this data structure?
Why this algorithm?
Why this complexity?
Why does it work?
Why not brute force?
Why not another approach?
```

---

# 14. Interview Communication Rule

> **Think aloud, but don't narrate every line of code.**

Explain the important decisions.

---

# 15. Final Interview Formula

```
Problem
  ↓
Approach
  ↓
Reason
  ↓
Optimization
  ↓
Correctness
  ↓
Complexity
  ↓
Edge Cases
  ↓
Code
```

> **Interviewers evaluate your reasoning, not just your final code.**