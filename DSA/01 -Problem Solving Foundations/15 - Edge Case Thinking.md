
---



```markdown


> **Edge cases are unusual or boundary inputs that can expose incorrect assumptions in an algorithm.**

---

## 1. Why Edge Cases Matter?

An algorithm may work for normal inputs but fail at boundaries.

Example:

```text
Normal:
[1, 5, 3, 8]

Edge:
[]
[1]
[-5, -2, -10]

```
## 2. Common Edge Cases

### Array

- Empty array
- One element
- All same values
- All negative
- Already sorted
- Reverse sorted
- Duplicates
- Very large values

### String

- Empty string
- One character
- All same characters
- Spaces
- Upper/lower case
- Special characters

### Numbers

- `0`
- Negative numbers
- Minimum/maximum integer
- Overflow

---

## 3. Boundary Conditions

Always check:

```
n = 0
n = 1
n = maximum constraint
```

For indexes:

```
0
n - 1
```

---

## 4. Example — Maximum

Incorrect:

```
int max = 0;
```

Fails for:

```
[-5, -2, -10]
```

Correct:

```
int max = arr[0];
```

assuming the array is non-empty.

---

## 5. Integer Overflow

Consider:

```
int mid = (left + right) / 2;
```

For large values, `left + right` can overflow.

Safer:

```
int mid = left + (right - left) / 2;
```

---

## 6. Edge Case Checklist

Before submitting:

```
□ Empty input
□ One element
□ Minimum input
□ Maximum input
□ Negative values
□ Zero
□ Duplicates
□ Already sorted
□ Reverse sorted
□ All equal
□ Overflow
□ Boundary indexes
```

Only test relevant cases.

---

## 7. Interview Habit

After explaining the algorithm, say:

> "I would also verify empty input, single-element input, duplicates, boundary values, and the maximum constraint."

This shows engineering maturity.

---

## 8. Quick Revision

> **Never test only the normal case. Test where your assumptions are most likely to break.**