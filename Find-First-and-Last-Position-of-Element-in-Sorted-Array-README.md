# leet-day86

# Problem Statement

Given an array of integers `nums` sorted in non-decreasing order, you need to find the starting and ending position of a given target value in the array. If the target value is not found in the array, return `[-1, -1]`.

We are required to implement an efficient algorithm with a runtime complexity of O(log n).

## Example

```
Input: nums = [5,7,7,8,8,10], target = 8
Output: [3,4]
Explanation: The target value 8 appears from index 3 to index 4 in the array.

Input: nums = [5,7,7,8,8,10], target = 6
Output: [-1,-1]
Explanation: The target value 6 is not present in the array, so we return [-1, -1].

Input: nums = [], target = 0
Output: [-1,-1]
Explanation: The array is empty, so we return [-1, -1].
```

# Approach

To find the starting and ending positions of the target value, we can perform two binary searches: one for finding the leftmost occurrence (the starting position) and the other for finding the rightmost occurrence (the ending position).

Here are the steps for our approach:

1. Define two helper functions, `findLeft` and `findRight`, for performing binary searches.
2. Initialize two variables, `left` and `right`, as the start and end indices of the array.
3. Initialize two variables, `leftMost` and `rightMost`, as -1. These variables will be used to store the leftmost and rightmost positions of the target value.
4. In the `findLeft` function, perform a binary search to find the leftmost occurrence of the target value. Update `leftMost` when the target value is found and continue the search in the left subarray.
5. In the `findRight` function, perform a binary search to find the rightmost occurrence of the target value. Update `rightMost` when the target value is found and continue the search in the right subarray.
6. After both binary searches are completed, if `leftMost` is less than or equal to `rightMost`, return `[leftMost, rightMost]`, indicating the range of positions where the target value is found. Otherwise, return `[-1, -1]` to indicate that the target value is not present in the array.

# Complexity Analysis

The time complexity of this approach is O(log n) because both `findLeft` and `findRight` perform binary searches.

The space complexity is O(1) as we use only a few extra variables to store indices and results.
