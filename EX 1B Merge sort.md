# EX 1B Merge Sort
## DATE:
## AIM:
To Write a Program for Implementing merge sort using python recursion

## Algorithm
1. If the array has more than one element, split it into two halves.
2. Recursively apply merge sort on both halves.
3. Compare elements of both halves and merge them into a sorted array.
4. Copy any remaining elements from the left or right half.
5. Return the fully sorted array.  

## Program:
```
def merge_sort(inp_arr):
    if len(inp_arr) < 2:               
        return inp_arr
    result = []                  
    mid = int(len(inp_arr) / 2)  
     
    y = merge_sort(inp_arr[:mid])       
    z = merge_sort(inp_arr[mid:])       
    i = 0
    j = 0
    while i < len(y) and j < len(z):
        if y[i] > z[j]:
            result.append(z[j])
            j += 1
        else:
            result.append(y[i])
            i += 1
    result += y[i:]             
    result += z[j:]             
    return result 
    
inp_arr=[]
n=int(input())
for i in range(n):
    inp_arr.append(int(input()))
print("Input Array:\n")
print(inp_arr)
print("Sorted Array:\n")
print(merge_sort(inp_arr))
```

## Output:
![Screenshot 2025-04-26 101850](https://github.com/user-attachments/assets/f83c9b4d-5876-4040-b28f-075a5d44c42d)




## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
