# Dynamic Programming
DP is enhanced recursion. How to identify if DP?
* If question asks for an optimal solution.
* In dp always choice, (like if include element or not)
* Most often when a single function calls two functions
* Ex: Max profit, max value of expression

  
DP = recursion + storage
Memoisation = storing results in cache, and retrieving that same information from the cache to speed up

If certain that dp is required, how to write algo:
1. Start by writing recursive solution
2. Don’t make matrix table first as it is used in only type of question

## Knapsack
Types of Questions:
Subset sum, Equal sum partition, Count of subset sum, Minimum subset sum difference, Target sum, number of subset given difference

Knapsack: bag that can contain items. 
Knapsack of three types:
1. Fractional (greedy, not dp): we can break the item into its smaller part to fill the knapsack
2. 0-1 Knapsack: we have to add item as a whole, cannot break down the item into smaller part
3. Unbounded knapsack: Unlimited supply of items. Can add the same item again and again

### Knapsack recursive Steps:
1. Make Choice Diagram
![image](https://github.com/MananDhiman/comp-sci-theory/assets/64782929/fa0d941c-25cc-4419-a2fb-6e4799d98256)

2. Base condition: Think of the smallest valid input
![image1](https://github.com/MananDhiman/comp-sci-theory/assets/64782929/9aefbbb2-b448-4817-a63f-8c047dceda00)
