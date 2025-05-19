# EX 6D BRUTE FORCE ALGORITHM
## DATE: 10.5.25
## AIM:
To write a python program using brute force method of searching for the given substring in the main string.




## Algorithm
1. Take lengths of the main string and the substring (l and l2).

2. Loop from i = 0 to l - l2 (to avoid index out of range).

3. At each index i, compare the substring string[i:i+l2] with the pattern.

4. If they match, print the index where the match is found.

5. Repeat for all positions to find all occurrences of the substring.
   

## Program:
```
/*
To implement the program using brute force method of searching for the given substring in the main string.


Developed by: LISIANA T
Register Number: 212222240053
*/
def match(string,sub):
    l=len(string)
    l2=len(sub)
    for i in range(l-l2+1):
        if string[i:i+l2]==sub:
            print("Found at index",i)
str1=input()
str2=input()


```

## Output:
![image](https://github.com/user-attachments/assets/514321c5-1f98-4556-b515-16c8f15cc564)


## Result:
Thus the above program was executed successfully for searching the substring at respective index.
