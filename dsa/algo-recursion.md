# Recursion
Advantages:
* combines elegance and complexity
* reduces need for complex loops and auxiliary DS
* can reduce time complexity with memoization
* works well with recursive structures like graphs and trees
Disadvantages:
* slow bcs cpu overhead
* out of memory error (stack overflow exception) (each recursive call is added to program stack)
* can be complex

**Call Stack: Each new function called gets added to top of stack, and when that function finishes execution it is popped, and next function resumes**

Each function call
1. What is base case?
2. Smallest amount of work in each iteration
