
---



```markdown


> **Debugging = Systematically finding and fixing the cause of incorrect program behavior.**

---

## 1. Debugging Mindset

Do not randomly change code.

Use:

```text
Observe
  ↓
Reproduce
  ↓
Isolate
  ↓
Understand
  ↓
Fix
  ↓
Retest

```
## 2. Step 1 — Reproduce

Find an input that consistently produces the bug.

```
Input
 ↓
Actual Output
 ↓
Expected Output
```

---

## 3. Step 2 — Find the First Wrong State

Do not focus only on the final wrong answer.

Trace:

```
Input
 ↓
State 1
 ↓
State 2
 ↓
State 3 ← first incorrect state
```

The bug usually exists before the first wrong state.

---

## 4. Step 3 — Check Assumptions

Ask:

- Is the input what I expect?
- Is the index valid?
- Is the variable initialized correctly?
- Is the loop condition correct?
- Is the update correct?
- Is there an off-by-one error?

---

## 5. Common DSA Bugs

### Off-by-one

```
for (int i = 0; i <= arr.length; i++)
```

Wrong because last valid index is:

```
arr.length - 1
```

Correct:

```
for (int i = 0; i < arr.length; i++)
```

---

### Wrong initialization

```
int max = 0;
```

May fail for all-negative arrays.

---

### Wrong loop update

```
i--
```

instead of:

```
i++
```

can cause incorrect behavior or an infinite loop.

---

### Wrong boundary

Binary Search is especially sensitive to:

```
left
right
mid
```

---

## 6. Debugging Tools

Use:

- Print statements
- IDE debugger
- Breakpoints
- Step Over
- Step Into
- Variable inspection
- Dry runs
- Test cases

---

## 7. Good Debugging Process

```
Bug
 ↓
Smallest failing input
 ↓
Dry run
 ↓
Locate first incorrect state
 ↓
Identify violated assumption
 ↓
Fix
 ↓
Test original + edge cases
```

---

## 8. Do Not Hide the Bug

Avoid simply adding conditions until the test passes.

Ask:

> **Why was the program wrong in the first place?**

---

## 9. Quick Revision

> **Debug the cause, not the symptom.**

> **Find the first point where the program's state becomes incorrect.**