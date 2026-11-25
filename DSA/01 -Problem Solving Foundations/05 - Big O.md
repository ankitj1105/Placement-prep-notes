
> **Big O describes an asymptotic upper bound on the growth of an algorithm's computational work.**

---

## 1. Why Big O?

We want to compare algorithms based on how they scale.

Example:

```text
Algorithm A → n operations
Algorithm B → n² operations 
```
For large `n`:

```
O(n) is generally more scalable than O(n²)
```

---

## 2. Basic Idea

Big O focuses on growth rather than exact runtime.

```
5n + 10
```

becomes:

```
O(n)
```

because constants and lower-order terms are ignored in asymptotic classification.

---

## 3. Rules

### Drop constants

```
O(5n) → O(n)
```

### Keep dominant term

```
O(n² + n + 10) → O(n²)
```

### Sequential work

```
O(n) + O(n) → O(n)
```

### Nested work

```
O(n) × O(n) → O(n²)
```

---

## 4. Common Growth Rates

```
O(1)
O(log n)
O(n)
O(n log n)
O(n²)
O(n³)
O(2ⁿ)
O(n!)
```

Lower growth generally scales better for large inputs.

---

## 5. Example

```
for (int i = 0; i < n; i++) {
}
```

```
O(n)
```

---

## 6. Important Clarification

Big O does **not automatically mean worst case**.

It is an asymptotic upper-bound notation.

Best, average and worst-case complexities can all be expressed using asymptotic notation.

---

## 7. Big O vs Exact Runtime

```
O(n)
```

does not mean:

```
n seconds
```

It describes how work grows with `n`.

---

## 8. Interview Traps

> Big O = Worst Case

❌ Incorrect as a definition.

> Nested loop = O(n²)

❌ Not always.

> O(100n) is much worse than O(n)

❌ Same asymptotic class.

> O(n + log n) = O(n)

✅ Correct.

---

## 9. Mental Model

```
Big O
  ↓
How fast can the work grow?
  ↓
As input becomes very large
```

---

## 10. One-Line Revision

> **Big O = asymptotic upper bound used to describe growth.**