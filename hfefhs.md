# Problem Set

---

## Easy

### 1. Find the Element that Appears Once

You are given an integer array `nums` where every element appears twice except for one element that appears once. Write a function to find the element that appears once.

#### Input:
```plaintext
nums = [4, 1, 2, 1, 2]
```

#### Output:
```plaintext
4
```

#### Input:
```plaintext
nums = [2, 2, 3, 3, 5, 5, 7]
```

#### Output:
```plaintext
7
```

---

### 2. Minimum Blocks to Add

You are given an array of `n` integers. You want to modify the array so that it is increasing, i.e., every element is at least as large as the previous element. On each move, you may increase the value of any element by one. What is the minimum number of moves required?

#### Input Format:
1. The first input line contains an integer `n`: the size of the array.
2. The second line contains `n` integers: `x_1, x_2, ..., x_n` the contents of the array.

#### Output Format:
Print the minimum number of moves.

#### Input:
```plaintext
5
3 2 5 1 7
```

#### Output:
```plaintext
5
```

#### Explanation:
To make the array non-decreasing, the heights need to be adjusted to `[3, 3, 5, 5, 7]`. A total of 5 blocks are added.

---

## Medium

### 1. BitWar

Once upon a time, there was a curious inventor named Max who loved exploring the secrets of numbers. One day, Max found two magical stones marked with numbers—one called "Left" and the other "Right." These stones represented a range of numbers in a mystical world. Max's task was to find a powerful energy hidden within this range, called "Bitwise AND."

To unlock the energy, Max had to take every number between the Left and Right stones and find their bitwise AND—a special way of combining numbers by matching their "binary bits."

For example:

When Max had the stones Left = 5 and Right = 7, he discovered the hidden energy was 4.
When both stones showed 0, the energy turned out to be 0.
When the stones showed 1 and 2147483647, the powerful energy was still 0!
Max realized the magic lay in how the numbers lined up in their binary form, and he knew the answer always depended on those mysterious bits.

### Problem:

Given two integers `Left` and `Right`, calculate the bitwise AND of all integers between `Left` and `Right` (inclusive).

#### Example:

#### Input:
```plaintext
Left = 5, Right = 7
```

#### Output:
```plaintext
4
```

---

### 2. Flame Hasira Permutation

A permutation of integers `1, 2, ..., n` is called **Flame Hasira** if there are no adjacent elements whose difference is exactly `1`.

Given an integer `n`, your task is to construct a **Flame Hasira** permutation if such a permutation exists. If there are multiple solutions, you can print any of them. If it is not possible to create a Flame Hasira permutation, print **"NO SOLUTION"**.

#### Input Format:
- A single integer `n` which represents the length of the permutation.

#### Output Format:
- If a Flame Hasira permutation exists, print any valid permutation of integers `1, 2, ..., n` where no two adjacent elements have a difference of `1`.
- If no such permutation exists, print **"NO SOLUTION"**.

#### Input:
```plaintext
5
```

#### Output:
```plaintext
4 2 5 3 1
```

#### Input:
```plaintext
3
```

#### Output:
```plaintext
NO SOLUTION
```

---

### 3. Way to Win

In a distant land, there were two powerful kingdoms. The first kingdom's king desired to conquer the second kingdom, but their battlefield was a vast matrix guarded by a mystical force. The only way for the king to conquer the land was to navigate the matrix in a perfect spiral pattern, starting from the top-left corner and spiraling inward.

The task is to help the king by printing out the exact path he should take for any battlefield size.

Spiral Movement:
Move right until you can't anymore.
Move down until you reach the bottom.
Move left until you can't anymore.
Move up until you're blocked.
Repeat the process inward, spiraling towards the center of the matrix

#### Input Format:
- A single integer n representing the size of the battlefield (a grid of size n x n).

#### Constraints
-  `1 <= n <= 10^3`

#### Output Format:
- Print the exact spiral path for the battlefield, starting from the top-left corner.

#### Example:

#### Input:
```plaintext
3
```
![alt text](<Screenshot 2024-10-14 014331.png>)

#### Output:
```plaintext
1->2->3->8->9->4->7->6->5
```

---

## Hard

### 1. Number Spiral Problem

A number spiral is an infinite grid whose upper-left square has the number 1. Your task is to find out the number in row `y` and column `x`.

![alt text](<material.png>)

#### Input Format:
- The first input line contains an integer `t`: the number of test cases.
- For each test case, the input contains two integers `y` and `x`.

#### Constraints:
- `1 ≤ t ≤ 10^5`
- `1 ≤ y, x ≤ 10^9`

#### Example:

#### Input:
```plaintext
3
2 3
1 1
4 2
```

#### Output:
```plaintext
8
1
15
```

---

### 2. X-Sum of Subarrays

You are given an array `nums` of `n` integers and two integers `k` and `x`. The x-sum of an array is calculated by the following procedure:

1. Count the occurrences of all elements in the array.
2. Keep only the occurrences of the top `x` most frequent elements. If two elements have the same number of occurrences, the element with the bigger value is considered more frequent.
3. Calculate the sum of the resulting array.

Return an integer array `answer` of length `n - k + 1` where `answer[i]` is the x-sum of the subarray `nums[i..i + k - 1]`.

#### Example:

#### Input:
```plaintext
nums = [1, 1, 2, 2, 3, 4, 2, 3], k = 6, x = 2
```

#### Output:
```plaintext
[6, 10, 12]
```

#### Explanation:
- For subarray `[1, 1, 2, 2, 3, 4]`, only elements `1` and `2` will be kept. Hence, `answer[0] = 1 + 1 + 2 + 2 = 6`.
- For subarray `[1, 2, 2, 3, 4, 2]`, only elements `2` and `4` will be kept. Hence, `answer[1] = 2 + 2 + 2 + 4 = 10`.
- For subarray `[2, 2, 3, 4, 2, 3]`, only elements `2` and `3` are kept. Hence, `answer[2] = 2 + 2 + 2 + 3 + 3 = 12`.
```
