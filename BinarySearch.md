
```markdown
# Binary Search: Iterative and Recursive Methods

## Introduction
Binary search is a fundamental searching technique that follows the divide-and-conquer strategy. It is specifically used to efficiently locate a target value within a sorted array or list. This article explains both the iterative and recursive approaches to binary search.

## Divide and Conquer Strategy
Divide and conquer is a problem-solving approach where a large problem is broken down into smaller subproblems. These subproblems are solved individually, and their solutions are combined to solve the original problem.

## Prerequisites for Binary Search
- **Sorted List**: The list or array must be sorted in either ascending or descending order.
- **Index Pointers**: Two pointers are needed—low (starting point) and high (ending point).

## Binary Search Process
Binary search works by repeatedly dividing the search interval in half. Here’s a simplified version of the binary search strategy:

### Initialize Bounds
- Start with two pointers: low and high.
- Low points to the first element, and high points to the last element of the array.

### Iterative Process
- While low is less than or equal to high, continue searching.
- Calculate the mid index as `(low + high) // 2`.
- Compare the target value with the element at the mid index:
  - If the target is equal to the mid element, return the mid index.
  - If the target is less than the mid element, update high to `mid - 1`.
  - If the target is greater than the mid element, update low to `mid + 1`.

### Termination
- If the search space is exhausted (i.e., low > high), the target is not present in the array.

## Binary Search Tree Representation
Binary search can be visualized as a binary tree:
- **Level 1**: [8]
- **Level 2**: [4, 12]
- **Level 3**: [2, 6, 10, 14]
- **Level 4**: [1, 3, 5, 7, 9, 11, 13, 15]

The values at the nodes are labeled from 1 to 15.

## Iterative Binary Search
The iterative approach uses a loop to perform binary search. Here is the algorithm:

```cpp
BinSearch(A, n, key)
{
    l = 1; h = n;
    while (l <= h)
    {
        mid = (l + h) / 2;
        if (key == A[mid])
            return mid;
        if (key < A[mid])
            h = mid - 1;
        else
            l = mid + 1;
    }
    return 0;
}
```

## Recursive Binary Search
The recursive approach uses function calls to perform binary search. Here is the algorithm:

```cpp
Algorithm RBinSearch(l, h, key)
{
    if (l == h)
    {
        if (A[l] == key)
            return l;
        else
            return 0;
    }
    else
    {
        mid = (l + h) / 2;
        if (key == A[mid])
            return mid;
        if (key < A[mid])
            return RBinSearch(l, mid - 1, key);
        else
            return RBinSearch(mid + 1, h, key);
    }
}
```

## Time Complexity
Binary search has a time complexity of `O(log n)`, where `n` is the number of elements in the array or list. This efficiency is due to the halving of the search space in each iteration or recursive call.

- **Best Case**: `O(1)` (the target value is at the middle).
- **Worst Case**: `O(log n)` (the target value is at a leaf node in the binary search tree).

## Usage
Binary search is commonly used in various applications, including the determination of the length of the longest common prefix using binary search. It can efficiently reduce the search space and is a fundamental technique in computer science.

## Conclusion
Binary search, with its iterative and recursive methods, is an efficient algorithm for searching a sorted array or list. Its divide-and-conquer approach makes it powerful, reducing the time complexity significantly compared to linear search.

## References
- [Binary Search - Iterative Method](https://youtu.be/C2apEw9pgtw?si=M1VaEdWssMjasFcL)
- [Binary Search - Recursive Method](https://youtu.be/uEUXGcc2VXM?si=8MW-TF891WLJWs2P)
```

