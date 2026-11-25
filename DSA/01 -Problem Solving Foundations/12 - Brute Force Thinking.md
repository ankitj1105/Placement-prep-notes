
---

```markdown

> **Brute Force means trying all relevant possibilities using the most straightforward correct approach.**

---

## 1. Why Learn Brute Force?

Brute force is important because it gives us a:

- Starting solution
- Correctness baseline
- Way to understand the problem
- Reference for optimization

Do not think:

> Brute force = bad solution.

Instead:

> Brute force = first correct solution that helps us discover a better solution.

---

## 2. Typical Process

```text
Understand Problem
       ↓
Build Brute Force
       ↓
Check Correctness
       ↓
Analyze Complexity
       ↓
Find Bottleneck
       ↓
Optimize

```
## 3. Example — Duplicate Elements

### Brute Force

Compare every pair.

```
for (int i = 0; i < n; i++) {
    for (int j = i + 1; j < n; j++) {
        if (arr[i] == arr[j]) {
            return true;
        }
    }
}
```

Time:

```
O(n²)
```

Space:

```
O(1)
```

---

## 4. Optimization

Ask:

> Why am I repeatedly searching for the same value?

Use a HashSet:

```
HashSet<Integer> set = new HashSet<>();

for (int x : arr) {
    if (set.contains(x)) {
        return true;
    }

    set.add(x);
}
```

Typical:

```
Time → O(n) average
Space → O(n)
```

---

## 5. Brute Force Checklist

Ask:

1. Can I try every possibility?
2. What is the simplest correct solution?
3. What is its complexity?
4. What work is repeated?
5. Can I store information?
6. Can I sort?
7. Can I use two pointers?
8. Can I use a HashMap/HashSet?
9. Can I use binary search?
10. Can I use a different data structure?

---

## 6. Brute Force Is Useful When

- Constraints are small
- Problem is simple
- You need a correctness baseline
- You are stuck
- You want to verify an optimized solution

---

## 7. Brute Force Is Not Enough When

Constraints are large and the brute-force complexity will not finish within the required time.

---

## 8. Interview Strategy

Never immediately jump to optimization.

A strong interview flow is:

```
Brute Force
    ↓
Complexity
    ↓
Bottleneck
    ↓
Observation
    ↓
Optimization
```

---

## 9. Quick Revision

> **Brute Force = simplest correct approach + starting point for optimization.**

> **First make it correct. Then make it fast.**