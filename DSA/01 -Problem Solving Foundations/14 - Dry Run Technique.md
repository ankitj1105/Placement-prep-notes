
---

# 📋 `14 - Dry Run Technique`

```markdown
# 14 - Dry Run Technique

> **Dry Run = Manually executing an algorithm step-by-step using a specific input.**

---

## 1. Why Dry Run?

Dry runs help us:

- Understand execution
- Find bugs
- Verify logic
- Check edge cases
- Explain solutions in interviews

---

## 2. Basic Method

Track:

- Variables
- Loop conditions
- Array/string changes
- Current result
- Important decisions

---

## 3. Example

```java
int sum = 0;

for (int i = 0; i < 3; i++) {
    sum += i;
}

```
Dry run:

|i|sum before|sum after|
|---|---|---|
|0|0|0|
|1|0|1|
|2|1|3|

Final:

```
sum = 3
```

---

## 4. Dry Run Table

For DSA, use:

|Step|i|j|Current Value|Result|
|---|---|---|---|---|

Only track variables that matter.

---

## 5. Array Dry Run

Example:

```
arr = [5, 2, 8]
```

Finding maximum:

```
Initial max = 5

2 > 5 ? No
8 > 5 ? Yes
max = 8
```

Answer:

```
8
```

---

## 6. Loop Dry Run

Always ask:

```
1. Initial value?
2. Condition?
3. Body execution?
4. Update?
5. Next iteration?
6. When does loop stop?
```

---

## 7. Debugging Through Dry Run

If actual output is wrong:

```
Expected
   ↓
Dry Run
   ↓
Find first incorrect state
   ↓
Inspect code responsible
```

The **first wrong state** is often more useful than looking at the final wrong output.

---

## 8. Interview Use

When explaining code:

```
Input
 ↓
Initial state
 ↓
Iteration 1
 ↓
Iteration 2
 ↓
...
 ↓
Final result
```

---

## 9. Quick Revision

> **Dry Run = Execute code manually without running it.**

Golden rule:

> **Track the state, not every character of the code.**