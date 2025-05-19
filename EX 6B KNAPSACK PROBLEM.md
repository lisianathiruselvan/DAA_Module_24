# EX 6B KNAPSACK PROBLEM
## DATE:
## AIM:
To demonstrate a python program using dynamic programming for 0/1 knapsack problem.



## Algorithm
1. If no items left or capacity W is 0, return 0 (base case).

2. If current item's weight > W, skip it and recurse with remaining items.

3. Otherwise, consider two choices:
– Include the item and add its value to the result of remaining capacity.
– Exclude the item and solve for the same capacity.

4. Take the maximum of including or excluding the item.

5. Return the result, which is the maximum value that fits within the given capacity.
   

## Program:
```
/*
To implement the program for 0/1 knapsack problem.


Developed by: LISIANA T
Register Number: 212222240053 
*/
def knapSack(W, wt, val, n):

     if n==0 or W==0:
         return 0
     if wt[n-1]>W:
         return knapSack(W, wt, val, n-1)
     return max(val[n-1]+knapSack(W-wt[n-1], wt, val, n-1),knapSack(W, wt, val, n-1))

x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))
n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
```

## Output:

![image](https://github.com/user-attachments/assets/160fec0d-4d91-4353-a047-ecb25358db46)



## Result:
Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity .
