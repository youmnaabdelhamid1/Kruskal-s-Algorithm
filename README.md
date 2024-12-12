
A: All Required Algorithms
1. Kruskal’s Algorithm
Kruskal's algorithm is used to find the Minimum Spanning Tree (MST) of a connected graph. The algorithm involves:

- Sorting all edges by weight.
- Iteratively adding the smallest edge to the MST, provided it doesn't form a cycle.
- Using a Union-Find (Disjoint Set Union) structure to efficiently check and manage cycles.


2. Supporting Algorithms
- Sorting edges by weight: Using an efficient sorting algorithm like Timsort with O(E log E) complexity.
- Union-Find Structure:
  - find: Finds the representative of a set.
  - union: Merges two sets.
 
  
B: Analyze in Detail
-> Time Complexity
1. Sorting Edges: O(E log E), where  E  is the number of edges.
2. Union-Find Operations:
   - Find: O(α(V)), where α is the inverse Ackermann function.
   - Union: O(α(V)).
   - Total for all edges: O(Eα(V)).
3. Overall Complexity: O(E log E + E α(V)), which simplifies to  O(E log E)  as log E dominates.

-> Space Complexity
- Storage for edges:O(E).
- Parent and rank arrays in Union-Find:O(V).
- Total: O(E + V).

-> Algorithm Correctness
- The algorithm ensures no cycles by checking the disjoint sets.
- The result is guaranteed to be a Minimum Spanning Tree because:
  - The graph is connected.
  - Edges are processed in increasing order of weight.
  - The Union-Find structure ensures minimal edge inclusion without cycles
