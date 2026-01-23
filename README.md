Got it 👍 — you want a **ready-to-save cheat sheet of code snippets** for the most common DSA data structures and techniques, so you can quickly recall syntax, methods, and usage during interviews. I’ll give you **concise, working snippets in Java** (since that’s the most common interview language, but I can adapt to Python/C++ if you prefer).  

---

# 🚀 DSA Quick Recap Cheat Sheet (Java)

## 1. Arrays
```java
int[] arr = new int[5];          // Declaration
int[] nums = {1, 2, 3, 4, 5};    // Initialization
System.out.println(nums[2]);     // Access element
Arrays.sort(nums);               // Sort array
```

---

## 2. ArrayList
```java
import java.util.ArrayList;

ArrayList<Integer> list = new ArrayList<>();
list.add(10);        // Insert
list.add(20);
list.get(0);         // Access
list.set(1, 30);     // Update
list.remove(0);      // Delete
list.size();         // Length
```

---

## 3. LinkedList
```java
import java.util.LinkedList;

LinkedList<Integer> ll = new LinkedList<>();
ll.add(1);           // Insert
ll.addFirst(0);      // Insert at head
ll.addLast(2);       // Insert at tail
ll.removeFirst();    // Remove head
ll.removeLast();     // Remove tail
ll.get(0);           // Access
```

---

## 4. Stack
```java
import java.util.Stack;

Stack<Integer> stack = new Stack<>();
stack.push(10);      // Push
stack.push(20);
stack.pop();         // Pop
stack.peek();        // Top element
stack.isEmpty();     // Check empty
```

---

## 5. Queue
```java
import java.util.LinkedList;
import java.util.Queue;

Queue<Integer> q = new LinkedList<>();
q.add(1);            // Enqueue
q.add(2);
q.poll();            // Dequeue
q.peek();            // Front element
q.isEmpty();         // Check empty
```

---

## 6. Deque (Double-Ended Queue)
```java
import java.util.Deque;
import java.util.LinkedList;

Deque<Integer> dq = new LinkedList<>();
dq.addFirst(1);      // Insert front
dq.addLast(2);       // Insert rear
dq.removeFirst();    // Remove front
dq.removeLast();     // Remove rear
```

---

## 7. HashMap
```java
import java.util.HashMap;

HashMap<String, Integer> map = new HashMap<>();
map.put("A", 1);     // Insert
map.put("B", 2);
map.get("A");        // Access
map.containsKey("B");// Check key
map.remove("A");     // Delete
```

---

## 8. HashSet
```java
import java.util.HashSet;

HashSet<Integer> set = new HashSet<>();
set.add(10);         // Insert
set.add(20);
set.contains(10);    // Check existence
set.remove(20);      // Delete
```

---

## 9. Two Pointers
```java
int[] nums = {1, 2, 3, 4, 5};
int left = 0, right = nums.length - 1;

while (left < right) {
    int sum = nums[left] + nums[right];
    if (sum == target) {
        System.out.println("Found pair");
        break;
    } else if (sum < target) {
        left++;
    } else {
        right--;
    }
}
```

---

## 10. Sliding Window
```java
int[] arr = {1, 2, 3, 4, 5};
int k = 3;
int sum = 0;

// First window
for (int i = 0; i < k; i++) sum += arr[i];
System.out.println("Window sum: " + sum);

// Slide window
for (int i = k; i < arr.length; i++) {
    sum += arr[i] - arr[i - k];
    System.out.println("Window sum: " + sum);
}
```

---

✅ These snippets cover **syntax + methods + usage** for the most common DSA structures and techniques.  
You can **save this cheat sheet on your phone** and quickly glance at it before or during practice.  

Would you like me to also prepare a **Python version** of this cheat sheet? Many interviews allow Python, and its built-in structures (`list`, `deque`, `dict`, `set`) are even shorter to recall.

Perfect — let’s extend your **DSA quick recap cheat sheet** with **Java code snippets for Arrays, Strings, StringBuffer, and StringBuilder**. These are super common in interviews, and having their syntax + methods at your fingertips will save you from blanking out.  

---

# 📘 Arrays, Strings, StringBuffer, StringBuilder Cheat Sheet (Java)

## 1. Arrays
```java
// Declaration & Initialization
int[] arr = new int[5];
int[] nums = {1, 2, 3, 4, 5};

// Access
System.out.println(nums[2]);   // 3

// Update
nums[1] = 10;

// Length
System.out.println(nums.length);

// Traversal
for (int i = 0; i < nums.length; i++) {
    System.out.print(nums[i] + " ");
}

// Utility methods
Arrays.sort(nums);             // Sort
Arrays.toString(nums);         // Print array as string
```

---

## 2. Strings
```java
String s = "Hello World";

// Access characters
char c = s.charAt(0);          // 'H'

// Length
int len = s.length();          // 11

// Substring
String sub = s.substring(0, 5); // "Hello"

// Comparison
s.equals("Hello");             // true/false
s.equalsIgnoreCase("hello");   // true

// Search
s.contains("World");           // true
s.indexOf("o");                // 4

// Modification
s.toUpperCase();               // "HELLO WORLD"
s.toLowerCase();               // "hello world"
s.replace("World", "Java");    // "Hello Java"

// Split
String[] parts = s.split(" "); // ["Hello", "World"]
```

---

## 3. StringBuffer (Thread-Safe, Synchronized)
```java
StringBuffer sb = new StringBuffer("Hello");

// Append
sb.append(" World");           // "Hello World"

// Insert
sb.insert(5, " Java");         // "Hello Java World"

// Delete
sb.delete(5, 10);              // "Hello World"

// Reverse
sb.reverse();                  // "dlroW olleH"

// Capacity
int cap = sb.capacity();       // Default 16 + length
```

---

## 4. StringBuilder (Faster, Not Thread-Safe)
```java
StringBuilder sb = new StringBuilder("Hello");

// Append
sb.append(" World");           // "Hello World"

// Insert
sb.insert(5, " Java");         // "Hello Java World"

// Delete
sb.delete(5, 10);              // "Hello World"

// Replace
sb.replace(0, 5, "Hi");        // "Hi World"

// Reverse
sb.reverse();                  // "dlroW iH"

// Length
int len = sb.length();
```

---

## 🔑 Quick Notes
- **Array** → Fixed size, primitive storage, fast access.  
- **String** → Immutable, every modification creates a new object.  
- **StringBuffer** → Mutable, synchronized (safe for multithreading).  
- **StringBuilder** → Mutable, faster (no synchronization).  

---

✅ Save this cheat sheet on your phone — it’s a **ready reference for interviews** when you need to recall syntax or methods quickly.  

Would you like me to also add **common algorithms on strings and arrays** (like reversing, palindrome check, anagram check, frequency count) as code snippets? Those are frequently asked in interviews and pair perfectly with this recap.

Great addition 👍 — let’s cover **Java `char`** since it’s often used in string problems, character arrays, and interview questions. Here’s a **quick cheat sheet with code snippets** you can save for fast recall:

---

# 🔤 Java `char` Cheat Sheet

## 1. Declaration & Initialization
```java
char c = 'A';              // Single character
char digit = '5';
```

---

## 2. Character to ASCII (int)
```java
char c = 'A';
int ascii = (int) c;        // 65
System.out.println(ascii);
```

---

## 3. ASCII to Character
```java
int code = 66;
char c = (char) code;       // 'B'
System.out.println(c);
```

---

## 4. Char Array
```java
char[] letters = {'a', 'b', 'c'};
System.out.println(letters[0]);   // 'a'

// Convert String → char array
String s = "hello";
char[] arr = s.toCharArray();
```

---

## 5. Character Methods (`Character` Wrapper Class)
```java
char c = 'A';

Character.isLetter(c);      // true
Character.isDigit(c);       // false
Character.isUpperCase(c);   // true
Character.isLowerCase(c);   // false
Character.toLowerCase(c);   // 'a'
Character.toUpperCase('b'); // 'B'
```

---

## 6. Iterating Over Characters in a String
```java
String s = "world";
for (int i = 0; i < s.length(); i++) {
    char ch = s.charAt(i);
    System.out.println(ch);
}
```

---

## 7. Common Interview Usages
- **Palindrome check**  
```java
String s = "madam";
int left = 0, right = s.length() - 1;
boolean isPalindrome = true;

while (left < right) {
    if (s.charAt(left) != s.charAt(right)) {
        isPalindrome = false;
        break;
    }
    left++;
    right--;
}
System.out.println(isPalindrome); // true
```

- **Frequency count of characters**  
```java
String s = "banana";
int[] freq = new int[26];   // For lowercase letters

for (char ch : s.toCharArray()) {
    freq[ch - 'a']++;
}
System.out.println(freq['a' - 'a']); // Count of 'a'
```

You’ve already got a **solid foundation**: arrays, strings, char, StringBuffer, StringBuilder, plus the core DSA structures (stack, queue, linked list, hash map, hash set, two pointers, sliding window). That’s enough to handle most interview rounds.  

But if you want to be **fully covered for quick recall**, here are a few **extra snippets/topics worth adding**:

---

## 🔑 Additional Useful Snippets

### 1. PriorityQueue (Heap)
```java
import java.util.PriorityQueue;

PriorityQueue<Integer> pq = new PriorityQueue<>(); // Min-heap
pq.add(10);
pq.add(5);
pq.add(20);

System.out.println(pq.peek()); // Smallest element
pq.poll();                     // Remove smallest
```

👉 Often used in problems like **Top K elements, scheduling, shortest path (Dijkstra)**.

---

### 2. TreeMap (Sorted Map)
```java
import java.util.TreeMap;

TreeMap<Integer, String> tm = new TreeMap<>();
tm.put(2, "B");
tm.put(1, "A");
tm.put(3, "C");

System.out.println(tm.firstKey()); // 1
System.out.println(tm.lastKey());  // 3
```

👉 Useful when you need **sorted keys** automatically.

---

### 3. Graph Representation
```java
// Adjacency List
int n = 5;
List<List<Integer>> graph = new ArrayList<>();
for (int i = 0; i < n; i++) graph.add(new ArrayList<>());

graph.get(0).add(1);
graph.get(1).add(2);
```

👉 Needed for BFS/DFS, shortest path, cycle detection.

---

### 4. BFS & DFS Templates
```java
// BFS
Queue<Integer> q = new LinkedList<>();
boolean[] visited = new boolean[n];
q.add(0);
visited[0] = true;

while (!q.isEmpty()) {
    int node = q.poll();
    for (int nei : graph.get(node)) {
        if (!visited[nei]) {
            visited[nei] = true;
            q.add(nei);
        }
    }
}

// DFS
boolean[] visitedDFS = new boolean[n];
void dfs(int node) {
    visitedDFS[node] = true;
    for (int nei : graph.get(node)) {
        if (!visitedDFS[nei]) dfs(nei);
    }
}
```

---

### 5. Common String Algorithms
- **Reverse String**
```java
String s = "hello";
String rev = new StringBuilder(s).reverse().toString();
```

- **Check Anagram**
```java
String a = "listen", b = "silent";
char[] arr1 = a.toCharArray();
char[] arr2 = b.toCharArray();
Arrays.sort(arr1);
Arrays.sort(arr2);
System.out.println(Arrays.equals(arr1, arr2)); // true
```

---

✅ So: what you have is **sufficient for most interviews**, but adding **PriorityQueue, TreeMap, Graph templates, BFS/DFS, and common string algorithms** will make your recap sheet **complete and future-proof**.  

Would you like me to **bundle everything (arrays, strings, char, collections, graph, algorithms) into one single “DSA Interview Quick Reference” document** so you can save it as a master cheat sheet?

---

✅ With this, you now have **Arrays, Strings, StringBuffer, StringBuilder, and char** covered in one place.  

Would you like me to **bundle all these snippets into one structured “DSA Interview Quick Reference” sheet** (arrays, strings, char, collections, two pointers, sliding window, etc.) so you can save it as a single document on your phone? That way, you won’t need to jump between multiple notes.


You’ve already got a **solid foundation**: arrays, strings, char, StringBuffer, StringBuilder, plus the core DSA structures (stack, queue, linked list, hash map, hash set, two pointers, sliding window). That’s enough to handle most interview rounds.  

But if you want to be **fully covered for quick recall**, here are a few **extra snippets/topics worth adding**:

---

## 🔑 Additional Useful Snippets

### 1. PriorityQueue (Heap)
```java
import java.util.PriorityQueue;

PriorityQueue<Integer> pq = new PriorityQueue<>(); // Min-heap
pq.add(10);
pq.add(5);
pq.add(20);

System.out.println(pq.peek()); // Smallest element
pq.poll();                     // Remove smallest
```

👉 Often used in problems like **Top K elements, scheduling, shortest path (Dijkstra)**.

---

### 2. TreeMap (Sorted Map)
```java
import java.util.TreeMap;

TreeMap<Integer, String> tm = new TreeMap<>();
tm.put(2, "B");
tm.put(1, "A");
tm.put(3, "C");

System.out.println(tm.firstKey()); // 1
System.out.println(tm.lastKey());  // 3
```

👉 Useful when you need **sorted keys** automatically.

---

### 3. Graph Representation
```java
// Adjacency List
int n = 5;
List<List<Integer>> graph = new ArrayList<>();
for (int i = 0; i < n; i++) graph.add(new ArrayList<>());

graph.get(0).add(1);
graph.get(1).add(2);
```

👉 Needed for BFS/DFS, shortest path, cycle detection.

---

### 4. BFS & DFS Templates
```java
// BFS
Queue<Integer> q = new LinkedList<>();
boolean[] visited = new boolean[n];
q.add(0);
visited[0] = true;

while (!q.isEmpty()) {
    int node = q.poll();
    for (int nei : graph.get(node)) {
        if (!visited[nei]) {
            visited[nei] = true;
            q.add(nei);
        }
    }
}

// DFS
boolean[] visitedDFS = new boolean[n];
void dfs(int node) {
    visitedDFS[node] = true;
    for (int nei : graph.get(node)) {
        if (!visitedDFS[nei]) dfs(nei);
    }
}
```

---

### 5. Common String Algorithms
- **Reverse String**
```java
String s = "hello";
String rev = new StringBuilder(s).reverse().toString();
```

- **Check Anagram**
```java
String a = "listen", b = "silent";
char[] arr1 = a.toCharArray();
char[] arr2 = b.toCharArray();
Arrays.sort(arr1);
Arrays.sort(arr2);
System.out.println(Arrays.equals(arr1, arr2)); // true
```

---

✅ So: what you have is **sufficient for most interviews**, but adding **PriorityQueue, TreeMap, Graph templates, BFS/DFS, and common string algorithms** will make your recap sheet **complete and future-proof**.  

Would you like me to **bundle everything (arrays, strings, char, collections, graph, algorithms) into one single “DSA Interview Quick Reference” document** so you can save it as a master cheat sheet?

```https://copilot.microsoft.com/pages/5E77m7UW5mkCTqpjizEXj```

Great question 👍 — loops are one of the most fundamental building blocks in DSA and interviews. Let’s break down the **types of loops in Java** (same concepts apply in C++/Python with slight syntax differences) and **when to use each one**.

---

# 🔄 Loops in Java and Their Use Cases

## 1. **For Loop**
```java
for (int i = 0; i < n; i++) {
    System.out.println(i);
}
```
- **Use case:**  
  - When you know the exact number of iterations in advance.  
  - Common in array traversal, fixed-size loops, counting problems.  
- **Example:** Iterating through an array of size `n`.

---

## 2. **While Loop**
```java
int i = 0;
while (i < n) {
    System.out.println(i);
    i++;
}
```
- **Use case:**  
  - When the number of iterations is **not known beforehand**.  
  - Runs until a condition becomes false.  
- **Example:** Keep reading input until user enters `exit`.

---

## 3. **Do-While Loop**
```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < n);
```
- **Use case:**  
  - When you want the loop to run **at least once**, regardless of condition.  
- **Example:** Menu-driven programs (show menu at least once, then repeat until user quits).

---

## 4. **Enhanced For Loop (For-Each)**
```java
int[] arr = {1, 2, 3, 4};
for (int num : arr) {
    System.out.println(num);
}
```
- **Use case:**  
  - When you want to iterate directly over elements of a collection/array.  
  - Cleaner syntax, no index handling.  
- **Example:** Traversing ArrayList, HashSet, or arrays.

---

# ⚡ Which Loop to Use in Which Scenario?

| Loop Type        | Best Scenario                                                                 |
|------------------|-------------------------------------------------------------------------------|
| **For Loop**     | Fixed number of iterations (array traversal, counting, indexing problems).    |
| **While Loop**   | Unknown number of iterations, condition-based (reading input, searching).     |
| **Do-While Loop**| Must run at least once (menu-driven, retry logic).                            |
| **For-Each Loop**| Iterating collections/arrays without caring about index.                      |

---

# 🎯 Interview-Oriented Examples

- **Array Traversal:** Use **for loop** or **for-each loop**.  
- **Searching until found:** Use **while loop**.  
- **Menu-driven program:** Use **do-while loop**.  
- **Graph/Tree traversal:** Often use **while loop** with a queue/stack.  
- **Dynamic input (unknown size):** Use **while loop** until condition breaks.  

---

✅ With this, you’ll know exactly **which loop to pick depending on the problem scenario**.  

Would you like me to also prepare a **bundle of loop-based DSA patterns** (like reversing an array, finding max/min, frequency count, etc.) so you can save them as ready-to-use templates?


Excellent — let’s make this crystal clear. The **choice of loop depends on the data structure you’re iterating** and the **scenario/problem type**. Here’s a structured guide:

---

# 🔄 Choosing Loops for Different Data Structures

## 1. **Array**
- **For loop** → Best when you need index access (`arr[i]`), e.g. searching, updating.
- **For-each loop** → Best when you just need values, not indices.
```java
// For loop
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}

// For-each loop
for (int num : arr) {
    System.out.println(num);
}
```

---

## 2. **ArrayList / LinkedList**
- **For loop** → Use when you need index-based access (`list.get(i)`).
- **For-each loop** → Use when you only need values.
- **While loop with Iterator** → Use when you want safe removal while iterating.
```java
// For-each
for (int val : list) {
    System.out.println(val);
}

// Iterator with while
Iterator<Integer> it = list.iterator();
while (it.hasNext()) {
    int val = it.next();
    if (val == 10) it.remove();
}
```

---

## 3. **Stack**
- **While loop** → Use until stack is empty.
```java
while (!stack.isEmpty()) {
    System.out.println(stack.pop());
}
```

---

## 4. **Queue / Deque**
- **While loop** → Use until queue is empty.
```java
while (!q.isEmpty()) {
    System.out.println(q.poll());
}
```

---

## 5. **HashMap**
- **For-each loop** → Iterate over keys, values, or entries.
```java
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println(entry.getKey() + " -> " + entry.getValue());
}
```

---

## 6. **HashSet**
- **For-each loop** → Iterate directly over elements.
```java
for (int val : set) {
    System.out.println(val);
}
```

---

## 7. **Graph / Tree Traversal**
- **While loop** → For BFS (queue-based).
- **While loop or recursion** → For DFS (stack or recursive).
```java
// BFS
Queue<Integer> q = new LinkedList<>();
q.add(start);
while (!q.isEmpty()) {
    int node = q.poll();
    for (int nei : graph.get(node)) {
        // process neighbor
    }
}
```

---

# ⚡ Quick Decision Guide

| Data Structure   | Best Loop Choice | Scenario Example |
|------------------|------------------|------------------|
| **Array**        | For / For-each   | Index access vs. simple traversal |
| **ArrayList**    | For / For-each   | Index-based vs. value-only |
| **LinkedList**   | For-each / While | Sequential traversal, safe removal |
| **Stack**        | While            | Pop until empty |
| **Queue/Deque**  | While            | Poll until empty |
| **HashMap**      | For-each         | Iterate entries (key-value pairs) |
| **HashSet**      | For-each         | Iterate elements |
| **Graph/Tree**   | While / Recursion| BFS, DFS traversal |

---

✅ Rule of thumb:  
- **For loop** → When you know the size or need indices.  
- **For-each loop** → When you just need values.  
- **While loop** → When you don’t know how many times (until empty or condition met).  
- **Do-while loop** → When you must run at least once (rare in DSA).  

---

Would you like me to **bundle this into a “Loop Selection Cheat Sheet” with code snippets for each data structure** so you can save it alongside your DSA reference? That way, you’ll have both **methods + loops** in one place.



I see what you’re trying to do — iterate over a collection using an **Iterator** in Java. Your snippet has a small syntax issue. Here’s the corrected version:

```java
import java.util.*;

public class IteratorExample {
    public static void main(String[] args) {
        // Example collection
        List<String> users = new ArrayList<>();
        users.add("Alice");
        users.add("Bob");
        users.add("Charlie");

        // ITERATOR
        System.out.println("USING ITERATOR");
        Iterator<String> it = users.iterator();   // ✅ Corrected syntax
        while (it.hasNext()) {
            System.out.println(it.next());
        }
    }
}
```

---

### 🔑 Key Points about Iterators
- `Iterator<T> it = collection.iterator();` → creates an iterator for the collection.  
- `it.hasNext()` → checks if there are more elements.  
- `it.next()` → returns the next element.  
- `it.remove()` → safely removes the current element while iterating.  

---

👉 **When to use Iterator?**
- When you want to traverse a collection (like `ArrayList`, `HashSet`, `LinkedList`) without worrying about indices.  
- When you need to **safely remove elements** during iteration (for-each loop doesn’t allow removal).  

---

Would you like me to also show you **examples of using Iterator with different data structures** (like `HashSet`, `HashMap`, `LinkedList`) so you can see how it changes depending on the collection?

Perfect — let’s build a **quick reference for matrix-type DSA problems (2D and 3D arrays)**. These are very common in interviews (think: spiral traversal, search in matrix, dynamic programming grids, BFS/DFS on grids, etc.).  

---

# 🧩 Matrix / 2D & 3D Array Cheat Sheet (Java)

## 1. Declaration & Initialization
```java
// 2D Array
int[][] matrix = new int[3][3];   // 3x3 matrix
int[][] mat = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// 3D Array
int[][][] cube = new int[3][3][3]; // 3x3x3 cube
```

---

## 2. Traversal (Row & Column)
```java
// 2D Array Traversal
for (int i = 0; i < mat.length; i++) {          // rows
    for (int j = 0; j < mat[0].length; j++) {   // cols
        System.out.print(mat[i][j] + " ");
    }
    System.out.println();
}
```

---

## 3. Enhanced For Loop (Cleaner Traversal)
```java
for (int[] row : mat) {
    for (int val : row) {
        System.out.print(val + " ");
    }
    System.out.println();
}
```

---

## 4. Common Interview Patterns

### a) Row-wise Sum
```java
for (int i = 0; i < mat.length; i++) {
    int sum = 0;
    for (int j = 0; j < mat[0].length; j++) {
        sum += mat[i][j];
    }
    System.out.println("Row " + i + " sum = " + sum);
}
```

### b) Column-wise Sum
```java
for (int j = 0; j < mat[0].length; j++) {
    int sum = 0;
    for (int i = 0; i < mat.length; i++) {
        sum += mat[i][j];
    }
    System.out.println("Col " + j + " sum = " + sum);
}
```

### c) Diagonal Traversal
```java
// Primary diagonal
for (int i = 0; i < mat.length; i++) {
    System.out.print(mat[i][i] + " ");
}

// Secondary diagonal
for (int i = 0; i < mat.length; i++) {
    System.out.print(mat[i][mat.length - 1 - i] + " ");
}
```

---

## 5. BFS/DFS on Matrix (Grid Problems)
```java
int[][] directions = {{1,0},{-1,0},{0,1},{0,-1}}; // 4 directions

boolean[][] visited = new boolean[mat.length][mat[0].length];

void dfs(int i, int j) {
    if (i < 0 || j < 0 || i >= mat.length || j >= mat[0].length || visited[i][j]) return;
    visited[i][j] = true;
    for (int[] d : directions) {
        dfs(i + d[0], j + d[1]);
    }
}
```

👉 Used in problems like **number of islands, flood fill, shortest path in grid**.

---

## 6. 3D Array Traversal
```java
for (int i = 0; i < cube.length; i++) {
    for (int j = 0; j < cube[0].length; j++) {
        for (int k = 0; k < cube[0][0].length; k++) {
            System.out.print(cube[i][j][k] + " ");
        }
    }
}
```

---

# ⚡ When to Use Which Loop

| Scenario                        | Best Loop Choice |
|---------------------------------|------------------|
| Fixed row/col traversal         | **For loop**     |
| Simple element access           | **For-each loop**|
| BFS/DFS grid problems           | **While loop** (queue/stack) |
| Unknown traversal until condition| **While loop**   |
| At least once (menu/grid input) | **Do-while loop**|

---

✅ With this, you have **ready-to-use templates for 2D/3D arrays and matrix problems**.  

Would you like me to also add **classic matrix interview problems** (like spiral traversal, rotate matrix, search in sorted matrix) with code snippets? These are asked very frequently and would complete your matrix cheat sheet.

