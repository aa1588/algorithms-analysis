# Insertion Sort

An efficient algorithm for sorting a small number of elements.

## Table of Contents

- [Pseudocode](##pseudocode)
- [Implementation](#implementation)
- [Loop Invariants (Proof for Correctness of Algorithm)](#loop-invariants-proof-for-correctness-of-algorithm)

## Pseudocode

```html
InsertionSort(A):
1    n = length(A)
2    for j = 2 to n
3        key = A[j]
4        //Insert "key" into the sorted sequence A[1 ... j-1]
5        i = j - 1
6        while i > 0 and A[i] > key
7            A[i + 1] = A[i]
8            i = i - 1
9        A[i + 1] = key
```

## Implementation

```java
     public static void insertionSort(int[] A) {
        int n = A.length;
        for (int j = 1; j < n; j++) { 
            int key = A[j];
            int i = j - 1;
            // Insert "key" into the sorted sequence A[0 ... j-1]
            while (i >= 0 && A[i] > key) {
                A[i + 1] = A[i];
                i--;
            }
            A[i + 1] = key;
        }
```

## Loop Invariants (Proof for Correctness of Algorithm)

Initialization: It is true prior to the first iteration of the loop.

Maintenance: If it is true before an iteration of the loop, it remains true before the next iteration.

Termination: When the loop terminates, the invariant gives us a useful property that helps show that the algorithm is correct.

[Watch Explanation on YouTube](https://www.youtube.com/watch?v=SElE4RlAji0)

[What is Loop Variant?](https://www.baeldung.com/cs/loop-invariant#:~:text=The%20requirement%20that%20the%20invariant,until%20the%20loop%20has%20ended.)