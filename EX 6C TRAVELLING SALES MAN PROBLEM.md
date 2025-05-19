# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE: 6.5.25
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm
1. List all vertices except the starting point s.

2. Generate all permutations of the remaining vertices (possible visiting orders).

3. For each permutation, calculate the total cost of the tour, starting and ending at s.

4. Keep track of the minimum cost among all possible tours.

5. Return the minimum cost, which is the optimal solution to the TSP.

## Program:
```
/*
To implement the program for TSP.


Developed by: LISIANA T
Register Number: 212222240053  
*/
from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
 
   #Write your code
    v=[]
    for i in range(V):
        if i!=s:
            v.append(i)
    mp=maxsize
    np=permutations(v)
    for i in np:
        k=s
        cp=0
        for j in i:
            cp+=graph[k][j]
            k=j
        cp+=graph[k][s]
        mp=min(cp,mp)
    return mp
   
 
 

if __name__ == "__main__":
 
        graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
        s = 0
        print(travellingSalesmanProblem(graph, s))
```

## Output:

![image](https://github.com/user-attachments/assets/cab10b63-a03d-45ed-b899-33b17a1374a3)


## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
