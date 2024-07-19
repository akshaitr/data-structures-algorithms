# Data-Structures-Algorithms
Fundamentals of data structures and algorithms applied to interviews.

## Time and space complexity

### Asymptotic analysis

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
- `O(|V|+|E|)`
  - Most commonly used when dealing with Graph algorithms

### Memoization

- Caching of (often expensive) function call results
- When we see the same input we just return the pre-computed value

```javascript
let cache = {};

function fibonacci(num) {
  if(num === 0) {
    return 0;
  } else if(num === 1) {
    return 1;
  }

  // Return cache value if it already exists
  if(cache[num]) {
    return cache[num];
  }

  // Cache the answer so later calls can use it
  cache[num] = fibonacci(num-1) * fibonacci(num-2);
  return cache[num];
}
```

### Analyzing recursive functions

  #### Iterative functions

  -   What you see is what you get
  -   Easier to reason about

  #### Recursive functions

  - Differ work in each call
  - Probabilistic/Combinatorial
  - Non-linear structure to analyze

Things to consider when analyzing a recursive function:
  - How deep does the recursive tree go?
  - Branching factor
  - Work per call (and worst work per call)
  - Total leaf nodes in the recursive tree
  - Look at the depth impact on the space complexity

