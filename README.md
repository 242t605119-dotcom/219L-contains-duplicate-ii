# LeetCode 219 - Contains Duplicate II

## Problem Description

Given an integer array `nums` and an integer `k`, determine whether there are two different indices `i` and `j` such that:

- `nums[i] == nums[j]`
- `abs(i - j) <= k`

In simple words, we need to check whether the same number appears twice within a distance of `k` indices.

## Example

Input:

nums = [1,2,3,1]
k = 3

The number `1` appears at indices `0` and `3`.

Their distance is:

3 - 0 = 3

Since `3 <= k`, the condition is satisfied.

Output:

True

## Approach

We use a dictionary to store the most recent index of each number.

While traversing the array, we check whether the current number has appeared before.

If it has appeared before, we calculate the difference between the current index and its previous index.

If the difference is less than or equal to `k`, we return `True`.

Otherwise, we update the number's index and continue.

## Algorithm

1. Create an empty dictionary called `seen`.
2. Traverse the array using both index and value.
3. If the current number already exists in the dictionary, calculate the index difference.
4. If the difference is at most `k`, return `True`.
5. Update the number with its current index.
6. Return `False` if no valid duplicate is found.

## Time Complexity

**O(n)**

The array is traversed once.

## Space Complexity

**O(n)**

The dictionary can store up to `n` different values.

## Key Concepts

- Hash Map
- Arrays
- Index Tracking
- Duplicate Detection
- Sliding Window Concept

## Author

T.nandhini
