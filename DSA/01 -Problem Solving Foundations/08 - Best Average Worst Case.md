
---

# 

```markdown


> Best, Average and Worst Case describe different input situations for an algorithm.

---

## 1. Best Case

The most favorable input.

Example: Linear Search

```text
[10, 20, 30, 40]

```
Target = `10`

Found immediately.

```
Best Case → O(1)
```

---

## 2. Worst Case

The least favorable input.

Target is:

- Last element
- Or not present

Then we may inspect all `n` elements.

```
Worst Case → O(n)
```

---

## 3. Average Case

Represents expected behavior under a specified model of inputs.

For linear search, under common assumptions:

```
Average Case → O(n)
```

But average-case analysis depends on assumptions about how inputs are distributed.

---

## 4. Example — Linear Search

```
for (int i = 0; i < n; i++) {
    if (arr[i] == target) {
        return i;
    }
}
```

```
Best Case    → O(1)
Average Case → O(n)
Worst Case   → O(n)
```

---

## 5. Do Not Confuse These Concepts

```
Best / Average / Worst
        ↓
Input scenario

O / Ω / Θ
        ↓
Asymptotic bounds
```

They answer different questions.

---

## 6. Big O Is Not "Worst Case"

Incorrect:

> Big O always means worst case.

Correct:

> Big O is an asymptotic upper-bound notation. Worst-case complexity is often expressed using Big O, but the two terms are not synonymous.

---

## 7. Best Case vs Ω

Do not assume:

```
Best Case = Ω
```

This is not generally true.

Best case is an input scenario.

Ω is a mathematical lower bound.

---

## 8. Why Worst Case Matters

Worst-case analysis tells us:

> How bad can the algorithm become for an input of size n?

This is useful when we need performance guarantees.

---

## 9. Interview Questions

- What is best-case complexity?
- What is worst-case complexity?
- What is average-case complexity?
- Why is worst-case analysis important?
- Is Big O always worst case?
- Is Ω always best case?
- Difference between worst case and upper bound?

---

## 10. Quick Revision

```
Best Case    → Most favorable input
Average Case → Expected behavior under assumptions
Worst Case   → Least favorable input

O  → Upper bound
Ω  → Lower bound
Θ  → Tight bound
```