# EX 5A Minimum Cost Path

## DATE : 28/03/2025

## AIM :

To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm :

1.Start at the top-left corner (0, 0) of the grid.

2.If you are already at the destination (R-1, C-1), return the cost of that cell.

3.If you're not at the destination.

4.From the current cell, you can move in three possible directions: Diagonally down-right, Down, Right.

5.Calculate the cost for each possible move and choose the minimum cost.

6.Repeat this process until you reach the destination cell (R-1, C-1).

7.Add the cost of the destination cell to the minimum cost found and return the result.   

8.Print the minimum cost to reach (R-1, C-1).

## Program :

### Developed by:NITEESH M
### Register Number: 212222230098

```
R = int(input())
C = int(input())

import sys
def minCost(cost, m, n):
    
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
                                minCost(cost, m-1, n),
                                minCost(cost, m, n-1) )
                                
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```

## Output :

![image](https://github.com/user-attachments/assets/b8633456-65bf-43bd-b68d-dbd55aabd46c)


## Result :

Thus the above program was executed successfully for finding the minimum cost.
