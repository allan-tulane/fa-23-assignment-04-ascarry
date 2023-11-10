# CMPS 2200 Assignment 4
## Answers

**Name:**______Abby Scarry___________


Place all written answers from `assignment-04.md` here for easier grading.

1a. Given N dollars, state a greedy algorithm for producing as few coins as possible that sum to N:

This greedy algorithm would involve first initializing the count of coins = 0, then repeatedly selecting the coin of the highest power of 2 that can fit (<=N), and then doing this repeatedly until reaching N.


1b. Prove that this algorithm is optimal by proving the greedy choice and optimal substructure properties.

The greedy algorithm above is optimal because the largest coin always makes the remaining change smaller the most. Since smaller denominations (2) can't combine to be larger than a larger coin, each greedy choice is the best one. This means that there will be a smaller problem to solve next, and that the best solution for that smaller amount, added to the coins already chosen, will always be the best solution. This satisfies optimal substructure property.

1c. What is the work and span of your algorithm?

Work and Span both = O(logN)
This is because each step decreases N by a power of 2

2a. Give a simple counterexample that shows that the greedy algorithm does not produce the fewest number of coins. 

A simple counterexample would be a situation where Fortuito's denominations are 1, 3, and 4, and you need to make change for 6 dollars. The greedy algorithm would involve choosing one coin of denomination 4, and then two coins of denomination 1, to get 6 dollars using three coins, but the optimal solution is to use two coins of denomination 3 to get 6 dollars with only two coins. Here, the greedy algorithm fails because it does not consider the combination of coins that results in the least number of coins used.

2b. Since you paid attention in Algorithms class, you realize that while this problem does not have the greedy choice property it does have an optimal substructure property. State and prove this property.

The optimal substructure property for the making change problem in Fortuito would mean  if you know the optimal way for  to make change for N dollars, then for any amount less than N, the solution included for that smaller amount must also be optimal

2c. Use this optimal substructure property to design a dynamic programming algorithm for this problem. If you used top-down or bottom-up memoization to avoid recomputing solutions to subproblems, what is the work and span of your approach?

W = (n*k)
S = O(n)