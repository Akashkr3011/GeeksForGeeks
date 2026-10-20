## 01. Sum Numbers in a String

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sum-of-numbers-in-string-1587115621/1)

### Problem Description

**Task:** Given a string s containing alphanumeric characters. You have to calculate the sum of all the numbers present in the string.

#### Examples

##### Example 1

- **Input:**
```text
s = "1abc23"
```
- **Output:**
```text
24
```
- **Explanation:** 1 and 23 are numbers in the string which is added to get the sum as 24.

##### Example 2

- **Input:**
```text
s = "geeks4geeks"
```
- **Output:**
```text
4
```
- **Explanation:** 4 is the only number, so the sum is 4.

#### Constraints

- **1.** `1 ≤ |s|≤ 10⁵The sum of Numbers ≤ 10⁵`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-20 17:09:51
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public static int findSum(String s) {
        int totalSum = 0;
        int currentNum = 0;

        for (int i = 0; i < s.length(); i++) {
            char ch = s.charAt(i);

            if (Character.isDigit(ch)) {
                // Build the current consecutive number
                currentNum = currentNum * 10 + (ch - '0');
            } else {
                // Add the accumulated number and reset
                totalSum += currentNum;
                currentNum = 0;
            }
        }

        // Add any remaining number at the end of the string
        totalSum += currentNum;

        return totalSum;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-20 17:07:38
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public static int findSum(String s) {
        int totalSum = 0;
        int currentNum = 0;

        for (int i = 0; i < s.length(); i++) {
            char ch = s.charAt(i);

            if (Character.isDigit(ch)) {
                // Build the current consecutive number
                currentNum = currentNum * 10 + (ch - '0');
            } else {
                // Add the accumulated number and reset
                totalSum += currentNum;
                currentNum = 0;
            }
        }

        // Add any remaining number at the end of the string
        totalSum += currentNum;

        return totalSum;
    }
}
```

*Generated on: 20/10/2026, 17:09:55*