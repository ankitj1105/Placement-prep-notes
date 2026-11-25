
---



```markdown


> **Big Omega, Ω(f(n)), represents an asymptotic lower bound.**

---

## 1. Meaning

Ω tells us that an algorithm requires at least a certain asymptotic amount of work.

Mental model:

```text
O  → Upper
Ω  → Lower
Θ  → Tight

```
## 2. Example

Finding the maximum in an unsorted array:

```
[4, 8, 2, 10, 5]
```

We must inspect the elements because any unexamined element could be larger.

Therefore:

```
Ω(n)
```

---

## 3. Important Distinction

Ω does NOT simply mean:

> Best Case

This is a common misconception.

Ω is a mathematical lower-bound notation.

Best-case complexity is a separate idea.

---

## 4. Example

Suppose:

```
T(n) = 3n + 5
```

Then:

```
Θ(n)
```

and therefore:

```
O(n)
Ω(n)
```

---

## 5. Comparison

|Notation|Meaning|
|---|---|
|O(f(n))|Upper bound|
|Ω(f(n))|Lower bound|
|Θ(f(n))|Tight bound|

---

## 6. Interview Trap

> Ω always means best case.

❌ Incorrect.

Ω describes a lower bound, not automatically a best-case scenario.

---

## 7. One-Line Revision

> **Ω = Asymptotic lower bound.**