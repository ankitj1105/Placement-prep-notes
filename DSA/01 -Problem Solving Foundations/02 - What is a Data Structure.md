````
> **Data Structure:** A way of organizing and storing data so that it can be accessed, processed, and modified efficiently.

---

## 1. Why Do We Need Data Structures?

A program usually works with data.

For example, a college application may need to store:

- Student ID
- Name
- Marks
- Department
- Attendance

As the amount of data grows, we need an efficient way to organize it.

The organization of data affects the efficiency of operations such as:

- Searching
- Insertion
- Deletion
- Access
- Updating
- Sorting
- Traversal

### Basic idea

```text
Data
  ↓
Need to organize it
  ↓
Choose a suitable Data Structure
  ↓
Perform operations efficiently
````

> **The goal of a data structure is not simply to store data, but to organize it in a way that makes required operations efficient.**

---

## 2. Simple Example

Suppose we have 1,000,000 student IDs.

### Unorganized data

```
52  →  17  →  91  →  4  →  73  → ...
```

Finding a particular ID may require checking many elements.

### Properly organized data

Depending on the requirement, we could use:

```
Array
HashSet
HashMap
Tree
```

Each structure provides different advantages.

Therefore:

> **There is no single "best" data structure. The correct choice depends on the operations we need.**

---

# 3. Data Structure vs Algorithm

These two concepts work together.

|Data Structure|Algorithm|
|---|---|
|Organizes data|Solves a problem|
|Defines how data is stored/managed|Defines steps to process data|
|Example: Array, HashMap|Example: Binary Search, BFS|

### Mental Model

```
Data Structure
      +
Algorithm
      ↓
Efficient Problem Solving
```

Example:

> Find whether an array contains duplicates.

Using:

```
Nested loops → O(n²)
```

Using:

```
HashSet → O(n) average
```

The algorithm and the data structure together determine the efficiency.

---

# 4. Classification of Data Structures

```
                    Data Structures
                          │
              ┌───────────┴───────────┐
              ↓                       ↓
           Linear                  Non-Linear
              │                       │
      ┌───────┼───────┐          ┌────┴────┐
      ↓       ↓       ↓          ↓         ↓
    Array   Stack   Queue       Tree      Graph
              │
          Linked List
              │
             Deque
```

Other important structures:

- HashMap
- HashSet
- Heap
- Trie
- Union-Find

---

# 5. Linear Data Structures

Elements are arranged sequentially.

```
A → B → C → D → E
```

Examples:

- Array
- Linked List
- Stack
- Queue
- Deque

---

# 6. Non-Linear Data Structures

Elements are organized hierarchically or through relationships.

### Tree

```
        A
       / \
      B   C
     / \
    D   E
```

### Graph

```
A ─── B
|   / |
|  /  |
C ─── D
```

Examples:

- Tree
- Graph
- Heap
- Trie

---

# 7. Array

An array stores elements using indexes.

```
int[] arr = {10, 20, 30, 40, 50};
```

```
Index:   0    1    2    3    4
         ↓    ↓    ↓    ↓    ↓
Value:  10   20   30   40   50
```

Access:

```
arr[2]
```

Result:

```
30
```

### Typical complexity

```
Access by index → O(1)
Search           → O(n)
```

Insertion/deletion can require shifting elements, so their cost depends on where the operation occurs.

---

# 8. Linked List

A linked list consists of nodes.

Each node contains:

```
Data + Reference to next node
```

Example:

```
[10 | next] → [20 | next] → [30 | next] → null
```

Unlike an array, nodes do not need to be stored next to one another.

### Typical characteristics

```
Access by position → O(n)
Search              → O(n)
```

Insertion/deletion can be efficient when the relevant node/position is already known.

> Do not say "Linked List insertion is always O(1)." Finding the position may itself take O(n).

---

# 9. Stack

A Stack follows:

> **LIFO — Last In, First Out**

```
       TOP
        ↓
      [30] ← removed first
      [20]
      [10]
```

Operations:

```
push()
pop()
peek()
```

### Applications

- Undo/Redo
- Browser history
- Function call stack
- Parentheses matching
- DFS

In Java, `Deque` with `ArrayDeque` is generally preferred for stack-like operations.

```
Deque<Integer> stack = new ArrayDeque<>();

stack.push(10);
stack.push(20);

int x = stack.pop();
```

---

# 10. Queue

A Queue follows:

> **FIFO — First In, First Out**

```
FRONT                         REAR
  ↓                             ↓
[10] → [20] → [30] → [40]
```

`10` leaves first.

Operations:

```
offer()
poll()
peek()
```

### Applications

- CPU scheduling
- Task processing
- BFS
- Printer queues
- Customer service systems

Java:

```
Queue<Integer> queue = new ArrayDeque<>();

queue.offer(10);
queue.offer(20);

int x = queue.poll();
```

---

# 11. Deque

Deque = **Double Ended Queue**

Insertion and deletion can happen from both ends.

```
FRONT                         REAR
  ↓                             ↓
[10] ↔ [20] ↔ [30] ↔ [40]
```

Java:

```
Deque<Integer> deque = new ArrayDeque<>();
```

Useful for:

- Sliding Window problems
- Stack operations
- Queue operations
- Monotonic Queue

---

# 12. HashMap

Stores data as:

```
Key → Value
```

Example:

```
HashMap<Integer, String> students = new HashMap<>();

students.put(101, "Ankit");
students.put(102, "Rahul");

System.out.println(students.get(101));
```

Output:

```
Ankit
```

Typical average-case:

```
put() → O(1)
get() → O(1)
remove() → O(1)
```

> These are average-case expectations, not an unconditional guarantee for every situation.

---

# 13. HashSet

Stores unique elements.

```
HashSet<Integer> set = new HashSet<>();

set.add(10);
set.add(20);
set.add(10);
```

Duplicates are not stored.

Useful for:

- Duplicate detection
- Membership checking
- Maintaining unique values

Typical average-case lookup:

```
O(1)
```

---

# 14. Tree

A tree represents hierarchical relationships.

```
          A
        /   \
       B     C
      / \
     D   E
```

Applications:

- File systems
- Organization hierarchy
- HTML DOM
- Search trees
- Database indexes

---

# 15. Heap / Priority Queue

A Heap is a specialized tree-based structure used to efficiently maintain priority.

Java:

```
PriorityQueue<Integer> pq = new PriorityQueue<>();
```

By default, Java's `PriorityQueue` is a min-priority queue.

Useful for:

- Top K problems
- Scheduling
- Dijkstra's algorithm
- Repeated minimum/maximum selection

---

# 16. Graph

A graph represents relationships between entities.

```
A ─── B
|     |
C ─── D
```

Applications:

- Google Maps
- Social networks
- Computer networks
- Flight routes
- Recommendation systems

---

# 17. Trie

A Trie is a tree-like structure mainly used for strings and prefixes.

Useful for:

- Autocomplete
- Prefix search
- Dictionary problems
- Word search

---

# 18. Union-Find

Also called:

> **Disjoint Set Union (DSU)**

Main operations:

```
find(x)
union(a, b)
```

Used for:

- Connected components
- Network connectivity
- Kruskal's algorithm

---

# 19. Abstract Data Type (ADT)

> **ADT describes what a data structure should do, not how it is implemented.**

Example:

### Stack ADT

```
push()
pop()
peek()
isEmpty()
```

It can be implemented using:

```
Array
Linked List
Deque
```

### Remember

```
ADT
 ↓
WHAT operations are supported?

Implementation
 ↓
HOW those operations are performed?
```

---

# 20. Static vs Dynamic Data Structures

### Static

Size is fixed.

```
int[] arr = new int[10];
```

### Dynamic

Can grow or shrink.

```
ArrayList<Integer> list = new ArrayList<>();
```

---

# 21. How to Choose a Data Structure?

Do not ask:

> "Which data structure is the best?"

Ask:

> **"What operations does my problem require?"**

|Requirement|Common Choice|
|---|---|
|Fast indexed access|Array / ArrayList|
|LIFO|Stack / Deque|
|FIFO|Queue / Deque|
|Key → Value|HashMap|
|Unique elements|HashSet|
|Sorted unique elements|TreeSet|
|Priority|PriorityQueue|
|Hierarchical data|Tree|
|Relationships|Graph|
|Prefix search|Trie|
|Connectivity|Union-Find|

---

# 22. Most Important DSA Thinking Pattern

```
Problem
   ↓
What operations are required?
   ↓
Choose Data Structure
   ↓
Choose Algorithm
   ↓
Analyze Time + Space
   ↓
Efficient Solution
```

This thought process is more important than memorizing definitions.

---

# 23. Common Interview Traps

### "Is Linked List always better than Array?"

No.

It depends on the operations.

### "Is HashMap always O(1)?"

No.

Typical average-case operations are O(1), but this is not an absolute guarantee.

### "Is Stack only implemented using arrays?"

No.

It can have multiple implementations.

### "What is the best data structure?"

There is no universal best data structure.

### "Is HashMap an algorithm?"

No.

It is a data structure.

---

# 24. Quick Revision

```
Array       → Indexed access
Linked List → Nodes connected by references
Stack       → LIFO
Queue       → FIFO
Deque       → Both ends
HashMap     → Key → Value
HashSet     → Unique values
Tree        → Hierarchical data
Graph       → Relationships
Heap        → Priority
Trie        → Prefix/String search
Union-Find  → Connectivity
```