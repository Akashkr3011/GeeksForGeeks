## 01. Selection Sort

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/selection-sort/1)

### Problem Description

**Task:** Given an array arr[], use selection sort to sort arr[] in increasing order.Examples :Input: arr[] = [4, 1, 3, 9, 7]

#### Examples

##### Example 1

- **Output:**
```text
[14, 20, 30, 31, 38]
```
- **Explanation:** Maintain sorted (in bold) and unsorted subarrays. Select 1. Array becomes 1 4 3 9 7. Select 3. Array becomes 1 3 4 9 7. Select 4. Array becomes 1 3 4 9 7. Select 7. Array becomes 1 3 4 7 9. Select 9. Array becomes 1 3 4 7 9.Input: arr[] = [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-22 12:14:51
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    void selectionSort(int[] arr) {
        // code here
        int n=arr.length;
        for(int curr=0;curr<n-1;curr++){
            int min_idx=curr;
            for(int j=curr+1;j<n;j++){
                if(arr[min_idx]>arr[j]){
                    min_idx=j;
                }
            }
            int temp=arr[curr];
            arr[curr]=arr[min_idx];
            arr[min_idx]=temp;
        }
    }
}
```

*Generated on: 22/10/2026, 12:15:21*