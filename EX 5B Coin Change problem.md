# EX 5B Coin Change Problem

## DATE : 28/03/2025

## AIM :

To compute the fewest number of coins that we need to make up the amount given.

## Algorithm :

1.Create an array (dp) to store the minimum number of coins needed for each amount.

2.Set dp[0] = 0 because no coins are needed to make 0.

3.Set all other values in dp to infinity (inf) because we don’t know the minimum coins yet.

4.For each coin in the given list of coins:Start from the coin value and go up to the target amount.

5.For each amount, update the dp array:If using the coin results in fewer coins than what is already stored, update it.

6.If dp[amount] is still infinity, return -1 (this means it’s not possible to make that amount with the given coins).

7.Otherwise, return the value in dp[amount], which is the minimum number of coins needed.

## Program :

### Developed by: NITEESH M
### Register Number:  212222230098

```
class Solution(object):
   def coinChange(self, coins, amount):
       
        dp = [float('inf')] * (amount + 1)
        dp[0]=0
        for coin in coins:
            for i in range(coin, amount + 1):
                dp[i] = min(dp[i], dp[i - coin] + 1)
        return dp[amount] if dp[amount]!=float('inf') else -1
      
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```

## Output :

![image](https://github.com/user-attachments/assets/cb149928-88a5-4e41-b4de-756781e27ab6)


## Result :

Thus the program was executed successfully for finding the minimum number of coins required to make amount.
