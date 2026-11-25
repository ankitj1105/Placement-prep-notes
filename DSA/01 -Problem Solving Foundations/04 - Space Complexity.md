
> **Space Complexity** describes how much memory an algorithm requires as the input size grows.

---

## 1. Why Do We Need Space Complexity?

An algorithm needs memory to store:

- Input data
- Variables
- Arrays
- Objects
- Data structures
- Function call information
- Temporary results

Two algorithms may have similar time complexity but use very different amounts of memory.

Therefore we analyze both:

```text
Time Complexity  → How much work?
Space Complexity → How much memory?
```

## 2. Time vs Space

|Complexity|Measures|
|---|---|
|Time Complexity|Growth of computational work|
|Space Complexity|Growth of memory usage|

Example:

```
int sum = 0;

for (int i = 0; i < n; i++) {
    sum += arr[i];
}
```

Time:

```
O(n)
```

Extra space:

```
O(1)
```

---

## 3. Input Space vs Auxiliary Space

### Input Space

Memory required to store the input itself.

### Auxiliary Space

Extra memory used by the algorithm **excluding the input**.

Example:

```
int sum = 0;

for (int x : arr) {
    sum += x;
}
```

If `arr` is already provided:

```
Input Space    → O(n)
Auxiliary Space → O(1)
```

> In interviews, always clarify whether the interviewer means **total space** or **auxiliary space**.

---

## 4. O(1) Auxiliary Space

Uses a constant amount of extra memory.

```
int max = arr[0];

for (int i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
        max = arr[i];
    }
}
```

Extra variables do not grow with `n`.

Therefore:

```
Auxiliary Space → O(1)
```

---

## 5. O(n) Auxiliary Space

Extra memory grows with input size.

```
int[] copy = new int[n];
```

The new array contains `n` elements.

Therefore:

```
Auxiliary Space → O(n)
```

---

## 6. In-Place Algorithm

An algorithm is commonly called **in-place** when it uses only a small amount of extra memory, typically O(1) auxiliary space.

Example:

```
for (int i = 0; i < n; i++) {
    // modify array directly
}
```

Advantages:

- Low memory usage
- Useful when memory is limited

Limitation:

- Sometimes extra memory can make the algorithm simpler or faster.

---

## 7. Recursion and Space

Recursion uses the function call stack.

Example:

```
void print(int n) {
    if (n == 0) return;

    print(n - 1);
}
```

For `n` recursive calls:

```
Call Stack
    ↓
n frames
```

Therefore:

```
Space → O(n)
```

> Recursion can use significant memory even if no array or collection is created.

---

## 8. Example

```
void fun(int n) {
    if (n == 0)
        return;

    fun(n - 1);
}
```

Time:

```
O(n)
```

Space:

```
O(n)
```

because of the recursion stack.

---

## 9. Multiple Variables

```
int a;
int b;
int c;
int d;
```

Number of variables is fixed.

Therefore:

```
O(1)
```

Even if there are 100 fixed variables:

```
O(100) = O(1)
```

---

## 10. Array Depending on n

```
int[] arr = new int[n];
```

Memory grows with `n`.

Therefore:

```
O(n)
```

---

## 11. Two Arrays

```
int[] a = new int[n];
int[] b = new int[n];
```

Total:

```
O(n) + O(n)
= O(2n)
= O(n)
```

---

## 12. 2D Array

```
int[][] matrix = new int[n][n];
```

Number of elements:

```
n × n = n²
```

Therefore:

```
O(n²)
```

---

## 13. Space Complexity Rules

```
Fixed variables       → O(1)
Array of size n       → O(n)
2D array n × n        → O(n²)
n recursive calls     → O(n)
HashMap with n items  → O(n)
```

---

## 14. Common Mistakes

### Mistake 1

> Input array of size n means auxiliary space is O(n).

Not necessarily.

If we only use a few variables:

```
Auxiliary Space = O(1)
```

### Mistake 2

> Recursion has O(1) space because no array is created.

Wrong.

The call stack consumes memory.

### Mistake 3

> Two arrays of size n means O(n²).

Wrong.

```
n + n = 2n = O(n)
```

---

## 15. Interview Questions

1. What is Space Complexity?
2. Time vs Space Complexity?
3. What is auxiliary space?
4. What is input space?
5. What is an in-place algorithm?
6. Why does recursion consume space?
7. What is the space complexity of an array of size n?
8. What is the space complexity of an n × n matrix?
9. Can an O(n) time algorithm use O(1) space?
10. Can an O(n) time algorithm use O(n) space?