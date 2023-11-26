# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
## STEP 1:
Start from the leftmost element of array[] and compare k with each element of array[] one by one.
## STEP 2:
If k matches with an element in array[] , return the index.
## STEP 3:
If k doesn’t match with any of elements in array[], return -1 or element not found.
## STEP 4:
End the program.


## Binary Search:
## STEP 1:
Set two pointers low and high at the lowest and the highest positions respectively.
## STEP 2:
Find the middle element mid of the array ie. arr[(low + high)/2]
## STEP 3:
If x == mid, then return mid.Else, compare the element to be searched with m.
## STEP 4:
If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
## STEP 5:
Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
## STEP 6:
Repeat steps 2 to 5 until low meets high
## STEP 7:
End the program
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by:SREEKUMAR S
RegisterNumber: 23008070
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
k = eval(input())
n=len(array)
array.sort()
print(array)
result=linearSearch(array,n,k)
if result != -1:
    print(f"Element found at index:  {result}")
else:
    print(f"Element not found ")


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:SREEKUMAR S
RegisterNumber:23008070 
'''
def binarysearch(array, k, low, high):
    while low<=high:
        mid=(low+high)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
    
    
array=eval(input())
array.sort()
k = eval(input())
result=binarysearch(array,k,0,len(array)-1)
print(array)
if result!=-1:
    print(f"Element found at index:  {result}")
else:
    print(f"Element not found")

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by:SREEKUMAR S
RegisterNumber:2308070 
'''
def binarysearch(arr, k, low, high):
    if low<=high:
        mid=(low+high)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return binarysearch(arr,k,mid+1,high)
        else:
            return binarysearch(arr,k,low,mid-1)
    else:
        return -1
    
    
arr = eval(input())
k = eval(input())

so=sorted(arr)
print(so)

result=binarysearch(so,k,0,len(arr)-1)
if result != -1:
    print(f"Element found at index:  {result}")
else:
    print(f"Element not found ")
```
## Sample Input and Output
![sort 1](https://github.com/guru14789/Search-Algorithm/assets/151705853/9af2f2b2-111f-4df8-9c42-45b48a06761e)

![sort 2](https://github.com/guru14789/Search-Algorithm/assets/151705853/3d452cbd-6337-4b86-9f5b-ab77981fa556)

![sort 3](https://github.com/guru14789/Search-Algorithm/assets/151705853/08fb447c-6048-4931-827d-16389c534bb4)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
