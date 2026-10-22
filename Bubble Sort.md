## 01. Bubble Sort

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/bubble-sort/1)

### Problem Description

**Task:** Given an array arr[]. Sort the array using bubble sort algorithm.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [4, 1, 3, 9, 7]
```
- **Output:**
```text
[1, 3, 4, 7, 9]Explanation: After Sorting the array in ascending order of their values is [1, 3, 4, 7, 9].
```

##### Example 2

- **Input:**
```text
arr[] = [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```
- **Output:**
```text
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]Explanation: Sort the array in ascending order of their values.
```

##### Example 3

- **Input:**
```text
arr[] = [1, 2, 3, 4, 5]
```
- **Output:**
```text
[1, 2, 3, 4, 5]Explanation: An array that is already sorted should remain unchanged after applying bubble sort.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-22 11:46:35
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public void bubbleSort(int[] arr) {
        // code here
        int n=arr.length;
        for(int i=0;i<n-1;i++){
            for(int j=0;j<n-i-1;j++){
                if(arr[j]>arr[j+1]){
                    int temp=arr[j];
                    arr[j]=arr[j+1];
                    arr[j+1]=temp;
                }
            }
        }
    }
}
```

*Generated on: 22/10/2026, 11:47:07*