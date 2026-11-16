# Comprehensive Technical Documentation: 28 DSA Problem-Solving Patterns

## Abstract & Engineering Context
This documentation encapsulates a rigorous approach to algorithmic problem-solving developed through extensive practice on platforms such as LeetCode and GeeksforGeeks, supplemented by advanced online curricula. By abstracting core problem-solving mechanics into **28 distinct Data Structures and Algorithms (DSA) patterns**, this framework transitions traditional brute-force methodologies into scalable, pattern-driven optimization techniques. Designed from a BTech Computer Science and Engineering perspective, this document serves as a reference architecture for recognizing structural invariants, optimizing time-space complexities, and designing robust software systems.

---

## 1. Linear & Sequential Array Manipulation Patterns

### 1.1 Two Pointers Pattern
*   **Core Concept:** Utilizing two index variables to traverse an iterable (usually linear data structures like arrays or strings) simultaneously, often from opposite ends or at different speeds, to reduce time complexity from $O(n^2)$ to $O(n)$.
*   **Use Cases:** Sorted array pair sums, palindrome validation, partitioning algorithms, removing duplicates.
*   **Complexity Profile:** Time: $O(n)$, Space: $O(1)$.

### 1.2 Sliding Window Pattern
*   **Core Concept:** Maintaining a dynamic or fixed-size window over a continuous subset of elements, updating the window's state incrementally as it shifts across the array rather than recomputing from scratch.
*   **Use Cases:** Maximum/minimum sum subarray of size $k$, longest substring without repeating characters, smallest subarray with a target sum.
*   **Complexity Profile:** Time: $O(n)$, Space: $O(k)$ or $O(1)$.

### 1.3 Prefix Sum Pattern
*   **Core Concept:** Precomputing cumulative sums of an array such that range sum queries can be executed in constant time $O(1)$.
*   **Use Cases:** Subarray sum equals $k$, range sum queries, equilibrium index identification.
*   **Complexity Profile:** Precomputation Time: $O(n)$, Query Time: $O(1)$, Space: $O(n)$.

### 1.4 Fast & Slow Pointers (Tortoise and Hare) Pattern
*   **Core Concept:** Deploying two pointers moving at different velocities (e.g., $1x$ and $2x$) to traverse data structures, primarily linked lists or arrays, to detect cycles or find specific structural midpoints.
*   **Use Cases:** Linked List Cycle Detection, finding the middle node of a linked list, happy number problem.
*   **Complexity Profile:** Time: $O(n)$, Space: $O(1)$.

---

## 2. Interval & Range Management Patterns

### 2.1 Merge Intervals Pattern
*   **Core Concept:** Handling overlapping intervals by sorting based on start times and merging intersecting boundaries to streamline temporal or spatial scheduling.
*   **Use Cases:** Meeting rooms, insert interval, interval intersection, merging overlapping intervals.
*   **Complexity Profile:** Time: $O(n \log n)$ due to sorting, Space: $O(n)$ for output.

### 2.2 Cyclic Sort Pattern
*   **Core Concept:** Iterating over arrays containing elements within a constrained range (e.g., $1$ to $n$) and placing each element at its designated index in-place.
*   **Use Cases:** Finding missing numbers, duplicate numbers, or first missing positive integer.
*   **Complexity Profile:** Time: $O(n)$, Space: $O(1)$.

---

## 3. Searching & Partitioning Patterns

### 3.1 Modified Binary Search Pattern
*   **Core Concept:** Adapting the standard divide-and-conquer binary search algorithm to handle rotated, duplicated, or monotonic-predicate search spaces.
*   **Use Cases:** Search in rotated sorted array, find peak element, minimum in rotated sorted array, square root computation.
*   **Complexity Profile:** Time: $O(\log n)$, Space: $O(1)$.

### 3.2 Binary Search on Answer Pattern
*   **Core Concept:** Framing optimization problems (minimizing maximums or maximizing minimums) as feasibility checks, applying binary search over the bounds of potential answers.
*   **Use Cases:** Capacity to ship packages within $D$ days, koko eating bananas, aggressive cows.
*   **Complexity Profile:** Time: $O(n \log(\text{range}))$, Space: $O(1)$.

---

## 4. Tree & Graph Traversal Patterns

### 4.1 Breadth-First Search (BFS) Pattern
*   **Core Concept:** Level-order traversal of hierarchical or networked data structures utilizing a Queue data structure to visit nodes layer by layer.
*   **Use Cases:** Shortest path in unweighted graphs, level order traversal of binary trees, word ladder.
*   **Complexity Profile:** Time: $O(V + E)$, Space: $O(W)$ where $W$ is the maximum width.

### 4.2 Depth-First Search (DFS) Pattern
*   **Core Concept:** Traversing graphs or trees by exploring as deep as possible along each branch before backtracking, implemented iteratively via an explicit Stack or recursively via the call stack.
*   **Use Cases:** Path finding, topological sorting, connected components, tree path sums.
*   **Complexity Profile:** Time: $O(V + E)$, Space: $O(H)$ where $H$ is the maximum height/depth.

### 4.3 Matrix Traversal (Flood Fill & Islands) Pattern
*   **Core Concept:** Treating 2D matrices as graphs where cells represent nodes and orthogonal/diagonal adjustments represent edges.
*   **Use Cases:** Number of islands, flood fill algorithm, surrounded regions, word search.
*   **Complexity Profile:** Time: $O(R \times C)$, Space: $O(R \times C)$ for recursion stack or visited matrix.

### 4.4 Topological Sort Pattern
*   **Core Concept:** Linear ordering of vertices in a directed acyclic graph (DAG) such that for every directed edge $u \to v$, vertex $u$ comes before $v$.
*   **Use Cases:** Course schedule, dependency resolution, build systems.
*   **Complexity Profile:** Time: $O(V + E)$, Space: $O(V + E)$.

---

## 5. Heap & Priority Queue Patterns

### 5.1 Two Heaps Pattern
*   **Core Concept:** Balancing two priority queues (a max-heap for the lower half and a min-heap for the upper half) to dynamically track statistical medians or continuous data streams.
*   **Use Cases:** Find median from data stream, sliding window median.
*   **Complexity Profile:** Time: $O(\log n)$ per insertion, $O(1)$ for median query; Space: $O(n)$.

### 5.2 Top 'K' Elements Pattern
*   **Core Concept:** Utilizing a min-heap or max-heap of size $k$ to maintain the top/smallest $k$ elements without sorting the entire dataset.
*   **Use Cases:** 'K' closest points to origin, top $k$ frequent elements, kth largest element in an array.
*   **Complexity Profile:** Time: $O(n \log k)$, Space: $O(k)$.

### 5.3 K-Way Merge Pattern
*   **Core Concept:** Merging $k$ sorted arrays or linked lists efficiently by leveraging a min-heap to always extract the smallest current element.
*   **Use Cases:** Merge k sorted lists, find kth smallest element in a sorted matrix.
*   **Complexity Profile:** Time: $O(n \log k)$, Space: $O(k)$.

---

## 6. Substring, Subsequence & String Matching Patterns

### 6.1 Sliding Window with Hash Map Pattern
*   **Core Concept:** Combining window bounds tracking with hash frequency maps to validate character constraints dynamically.
*   **Use Cases:** Longest substring with $k$ distinct characters, permutation in a string, minimum window substring.
*   **Complexity Profile:** Time: $O(n)$, Space: $O(k)$ or character set size.

### 6.2 Monotonic Stack / Queue Pattern
*   **Core Concept:** Maintaining a stack or queue whose elements are strictly increasing or decreasing, allowing efficient retrieval of the next greater or smaller elements.
*   **Use Cases:** Next greater element, daily temperatures, largest rectangle in histogram, trapping rain water.
*   **Complexity Profile:** Time: $O(n)$, Space: $O(n)$.

### 6.3 String Anagrams & Permutations Pattern
*   **Core Concept:** Frequency signature matching using fixed-size arrays or hash maps to check string identity invariant properties.
*   **Use Cases:** Group anagrams, find all anagrams in a string, valid anagram.
*   **Complexity Profile:** Time: $O(n \times m)$ or $O(n)$, Space: $O(1)$ for fixed character sets.

---

## 7. Recursion & Backtracking Patterns

### 7.1 Backtracking Pattern
*   **Core Concept:** Incrementally building candidates to solutions and abandoning a candidate ("backtracking") as soon as it is determined that the candidate cannot lead to a valid solution.
*   **Use Cases:** Permutations, combinations, subsets, N-Queens problem, Sudoku solver.
*   **Complexity Profile:** Time: Exponential $O(2^n)$ or $O(n!)$, Space: $O(n)$ call stack depth.

---

## 8. Dynamic Programming & Memoization Patterns

### 8.1 0/1 Knapsack Pattern
*   **Core Concept:** Solving optimization problems where items have weights and values, choosing whether to include or exclude an item under capacity constraints.
*   **Use Cases:** Partition equal subset sum, target sum, subset sum problem.
*   **Complexity Profile:** Time: $O(N \times W)$, Space: $O(N \times W)$ or optimized to $O(W)$.

### 8.2 Unbounded Knapsack Pattern
*   **Core Concept:** Variant of the knapsack problem where items can be selected an unlimited number of times.
*   **Use Cases:** Coin change, rod cutting, minimum coin interchange.
*   **Complexity Profile:** Time: $O(N \times W)$, Space: $O(W)$.

### 8.3 Fibonacci Numbers & Linear Recurrence Pattern
*   **Core Concept:** Breaking problems down into overlapping subproblems governed by linear recurrence relations, optimized via tabulation or memoization.
*   **Use Cases:** House robber, climb stairs, min cost climbing stairs.
*   **Complexity Profile:** Time: $O(n)$, Space: $O(1)$ with rolling variables.

### 8.4 Longest Common Substring / Subsequence Pattern
*   **Core Concept:** Tabulating sequential matches between two strings or sequences to evaluate structural similarity.
*   **Use Cases:** Longest common subsequence, edit distance, longest palindromic subsequence, distinct subsequences.
*   **Complexity Profile:** Time: $O(m \times n)$, Space: $O(m \times n)$ or $O(\min(m, n))$.

### 8.5 Palindromic Substring DP Pattern
*   **Core Concept:** Expanding around centers or utilizing 2D boolean tables to evaluate palindromic properties across ranges.
*   **Use Cases:** Longest palindromic substring, palindromic substrings count.
*   **Complexity Profile:** Time: $O(n^2)$, Space: $O(n^2)$ or $O(1)$ space with center expansion.

---

## 9. Advanced Data Structures & Graph Algorithms

### 9.1 Trie (Prefix Tree) Pattern
*   **Core Concept:** Tree-based data structure optimized for storing and retrieving strings by their prefixes, enabling efficient prefix searches.
*   **Use Cases:** Implement Trie, word search II, autocomplete systems, replace words.
*   **Complexity Profile:** Time: $O(m)$ per word insertion/search ($m$ = word length), Space: $O(ALPHABET\_SIZE \times N \times M)$.

### 9.2 Disjoint Set Union (DSU / Union-Find) Pattern
*   **Core Concept:** Tracking partition of a set into disjoint subsets, supporting rapid union and find operations optimized with path compression and union by rank.
*   **Use Cases:** Kruskal's minimum spanning tree algorithm, number of connected components, redundant connection, friend circles.
*   **Complexity Profile:** Time: $O(\alpha(n))$ nearly constant per operation, Space: $O(n)$.

### 9.3 Bitwise Manipulation Pattern
*   **Core Concept:** Exploiting binary representation properties and bitwise operators (XOR, AND, OR, Shifts) for low-level computational optimization and state compression.
*   **Use Cases:** Single number, counting bits, power of two, subsets using bitmasking.
*   **Complexity Profile:** Time: $O(1)$ per operation, Space: $O(1)$.

### 9.4 Greedy Algorithm Pattern
*   **Core Concept:** Making locally optimal choices at each stage with the intent of finding a global optimum.
*   **Use Cases:** Activity selection, interval scheduling, jump game, gas station problem.
*   **Complexity Profile:** Time: $O(n \log n)$ or $O(n)$, Space: $O(1)$.

---

## Summary Matrix

| Category | Pattern Name | Primary Data Structure | Optimal Time Complexity |
| :--- | :--- | :--- | :--- |
| **Array/String** | Two Pointers | Array / String | $O(n)$ |
| **Array/String** | Sliding Window | Array / String | $O(n)$ |
| **Array/String** | Prefix Sum | Array | $O(1)$ Query |
| **Pointers** | Fast & Slow Pointers | Linked List / Array | $O(n)$ |
| **Intervals** | Merge Intervals | Array | $O(n \log n)$ |
| **Sorting** | Cyclic Sort | Array | $O(n)$ |
| **Search** | Modified Binary Search | Array | $O(log n)$ |
| **Search** | Binary Search on Answer | Search Space | $O(n \log(\text{range}))$ |
| **Graph/Tree** | Breadth-First Search | Queue / Graph | $O(V + E)$ |
| **Graph/Tree** | Depth-First Search | Stack / Graph | $O(V + E)$ |
| **Graph/Tree** | Matrix Traversal | 2D Array | $O(R \times C)$ |
| **Graph/Tree** | Topological Sort | DAG / Graph | $O(V + E)$ |
| **Heaps** | Two Heaps | Heap / Priority Queue | $O(\log n)$ |
| **Heaps** | Top 'K' Elements | Heap | $O(n \log k)$ |
| **Heaps** | K-Way Merge | Heap | $O(n \log k)$ |
| **String** | Sliding Window Hash Map | Hash Map / String | $O(n)$ |
| **Stack** | Monotonic Stack/Queue | Stack | $O(n)$ |
| **String** | Anagrams & Permutations | Hash Map / Array | $O(n)$ |
| **Recursion** | Backtracking | Call Stack | Exponential |
| **DP** | 0/1 Knapsack | 2D/1D Array | $O(N \times W)$ |
| **DP** | Unbounded Knapsack | 1D Array | $O(N \times W)$ |
| **DP** | Linear Recurrence | Array / Variables | $O(n)$ |
| **DP** | LCS / Substring | 2D Array | $O(m \times n)$ |
| **DP** | Palindromic Substring | 2D Array / Expansion | $O(n^2)$ |
| **Advanced** | Trie | Tree | $O(m)$ |
| **Advanced** | DSU (Union-Find) | Disjoint Set | $O(\alpha(n))$ |
| **Advanced** | Bitwise Manipulation | Integer | $O(1)$ |
| **Advanced** | Greedy | Array | $O(n \log n)$ |

---
*Signed,*  
*BTech Computer Science and Engineering Portfolio Document.*