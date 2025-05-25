# EX 5C Kadane's Algorithm

## DATE : 28/03/2025

## AIM :

To write a python program to find the maximum contiguous subarray.

## Algorithm :

1.Set up two variables:

2.max_till_now starts with the first element of the array (it holds the best sum found so far).

3.max_ending starts at 0 (it tracks the current subarray sum).

4.Loop through the array:

5.Add each element to max_ending.

6.If max_ending becomes negative, reset it to 0 (we don’t want negative sums).

7.If max_ending is larger than max_till_now, update max_till_now to be the value of max_ending.

8.Return the value of max_till_now at the end. This is the largest sum of a contiguous subarray.   

## Program :

### Developed by: NITEESH M
### Register Number:  212222230098

```
def maxSubArraySum(a,size):
    
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
    
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```

## Output :

![image](https://github.com/user-attachments/assets/a3cab0c3-35e1-456e-aafe-b18dac632d29)


## Result :

Thus the program was executed successfully for finding the maximum contiguous sum of subarray.
