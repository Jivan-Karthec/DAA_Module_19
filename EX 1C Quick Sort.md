# EX 1C Quick Sort
## DATE:
## AIM:
 To Write a python program to implement quick sort on the given values and print the sorted list and pivot value of each iteration

## Algorithm
1. Select a pivot element from the array (commonly the first or last element).
2. Partition the array into two subarrays: elements less than pivot and elements greater than or equal to pivot.
3. Place the pivot between the two subarrays at its correct position.
3. Recursively apply Quick Sort to the left subarray.
4. Recursively apply Quick Sort to the right subarray. 

## Program:
```
/*
Write a python to implement Quick sort using the first element as pivot value
Developed by: Jivan Karthec B S
Register Number: 212222100017
*/
```
```
def qs(l,r,nums):
    if l<r:
        pi=partition(l,r,nums)
        qs(l,pi-1,nums)
        qs(pi+1,r,nums)
def partition(l,r,nums):
    pivot,i,j=nums[l],l,r
    print("Pivot: ",pivot)
    while True:
        while i<=j and nums[i]<=pivot:
            i+=1
        while i<=j and nums[j]>=pivot:
            j-=1
        if i<=j:
            nums[i],nums[j]=nums[j],nums[i]
        else:
            break
    nums[j],nums[l]=nums[l],nums[j]
    return j
n=int(input())
nums=[int(input()) for i in range(n)]
qs(0,n-1,nums)
print("Sorted array:",nums)
 ```

## Output:
![image](https://github.com/user-attachments/assets/bea1049f-3a93-46f6-b3a0-d3bd91fa712f)





## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
