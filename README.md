# Data-Structures-Algorithms
Fundamentals of data structures and algorithms applied to interviews.

## Time and space complexity

### Asymptotic Analysis

- How does my function perform asymptotically? As we limit to a large value of input, how does my function perform?
- Constant time `O(1)`
  - The most common time complexity for any single line of code you will ever write
  - Constant time does not mean “instant,” it just means that the operation’s runtime does not scale with a scaling of the input’s size
- Logarithmic time `O(logn)`
  - Often comes up when dealing with tree structures
- Linear time `O(n)`
  - Often comes up when dealing with non nested passes and data structures like Linked lists, Arrays
- `O(nlogn)`
  - Divide and conquer algorithm that satisfies the recurrence such as merge sort
  - Often comes up when dealing with `n` size structure having `logn` work at each element
- Factorial time `O(n!)`
  - Often comes up with problems dealing with permutations
