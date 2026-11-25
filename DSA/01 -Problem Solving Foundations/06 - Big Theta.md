
---

> **Big Theta, Θ(f(n)), represents a tight asymptotic bound.**

---

## 1. Meaning

If an algorithm grows at the same asymptotic rate from both upper and lower bounds:

```text
Θ(f(n))

```
can be used.

Mental model:

```
O  → Upper bound
Ω  → Lower bound
Θ  → Tight bound
```

---

## 2. Example

Suppose:

```
T(n) = 3n + 5
```

For large `n`:

```
T(n) grows linearly
```

Therefore:

```
Θ(n)
```

---

## 3. Example — Find Maximum

Finding the maximum in an unsorted array requires examining every element.

Therefore:

```
Upper Bound → O(n)
Lower Bound → Ω(n)
```

Hence:

```
Θ(n)
```

---

## 4. Relationship

```
Ω(f(n)) ≤ T(n) ≤ O(f(n))
```

When both bounds have the same asymptotic growth:

```
T(n) = Θ(f(n))
```

---

## 5. Example

```
T(n) = n² + 5n + 10
```

Dominant term:

```
n²
```

Therefore:

```
Θ(n²)
```

---

## 6. Big O vs Big Theta

|Big O|Big Theta|
|---|---|
|Upper bound|Tight bound|
|Can be loose|Asymptotically exact growth|
|O(n²) can describe an O(n) algorithm|Θ(n) describes linear growth|

---

## 7. Important Point

If:

```
T(n) = Θ(n)
```

then it is also:

```
O(n)
```

and:

```
Ω(n)
```

---

## 8. Interview Question

### What is the difference between O and Θ?

> O describes an asymptotic upper bound, while Θ describes a tight asymptotic bound.

---

## 9. One-Line Revision

> **Θ = Tight asymptotic growth.**