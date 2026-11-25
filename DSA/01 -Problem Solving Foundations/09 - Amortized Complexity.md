
---


```markdown

> **Amortized analysis studies the average cost per operation over a sequence of operations.**

---

## 1. Why Do We Need Amortized Analysis?

Some operations are usually cheap but occasionally expensive.

Example:

```text
Dynamic Array

```
Most insertions:

```
O(1)
```

But when the array becomes full, it may need to:

1. Allocate a larger array
2. Copy existing elements
3. Insert the new element

That particular operation can cost:

```
O(n)
```

However, expensive resizing does not happen every time.

---

## 2. Dynamic Array Example

Suppose capacity doubles:

```
Capacity:

1
↓
2
↓
4
↓
8
↓
16
↓
...
```

Most insertions:

```
O(1)
```

Occasional resize:

```
O(n)
```

Over many insertions, the average cost per insertion is:

```
O(1) amortized
```

---

## 3. Important Distinction

```
Worst-case individual operation
        ↓
May be O(n)

Amortized cost over many operations
        ↓
May be O(1)
```

Therefore:

> Amortized O(1) does NOT mean every operation takes O(1).

---

## 4. Example

Suppose we perform:

```
n insertions
```

The total copying caused by doubling is approximately:

```
1 + 2 + 4 + 8 + ... < 2n
```

Therefore total work is:

```
O(n)
```

For `n` insertions:

```
Total → O(n)
```

Average per insertion:

```
O(n) / n
= O(1)
```

---

## 5. Common Examples

Amortized analysis appears in:

- Dynamic arrays
- ArrayList
- Hash table resizing
- Union-Find
- Some data structure operations

---

## 6. Amortized vs Average Case

These are not the same.

### Average Case

Depends on a probability/distribution model for inputs.

### Amortized Analysis

Considers the total cost over a sequence of operations and spreads expensive operations across the sequence.

---

## 7. Three Common Amortized Techniques

### Aggregate Method

Calculate total cost of a sequence and divide by number of operations.

### Accounting Method

Cheap operations are charged extra to save credit for future expensive operations.

### Potential Method

Use a potential function to represent stored "energy" that can pay for future expensive operations.

For placement-level DSA, the aggregate idea is usually the easiest starting point.

---

## 8. Interview Question

### Can an operation be O(n) worst case but O(1) amortized?

Yes.

Example:

```
Dynamic Array insertion
```

Most operations are O(1), while occasional resizing is O(n).

Over a long sequence:

```
Amortized → O(1)
```

---

## 9. Quick Revision

```
Amortized Analysis
        ↓
Sequence of operations
        ↓
Total cost
        ↓
Average cost per operation
```

> **Amortized O(1) ≠ every operation is O(1).**