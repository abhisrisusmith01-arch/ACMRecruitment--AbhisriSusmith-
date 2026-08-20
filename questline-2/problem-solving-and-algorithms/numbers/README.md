# Problem Solving & Algorithms - Numbers

## Problem 1: Palindrome Number

### Thought Process
   The number is mathematically reversed digit by digit using modulo (`% 10`) and integer division (`// 10`). Comparing the reversed integer directly against the stored original integer determines if it is a palindrome.

### Algorithm
1. Start
2. Store the original number in a variable `original = x` to preserve its initial value.
3. Initialize `reversed_num = 0`.
4 While `x > 0`:
   * Extract the last digit: `digit = x % 10`.
   * Append the digit to `reversed_num`: `reversed_num = (reversed_num * 10) + digit`.
   * Remove the last digit from `x`: `x //= 10`.
5. Return `True` if `original == reversed_num`, otherwise `False`.
6. Stop
---

## Problem 2: Integer to Roman

### Thought Process
Roman numerals represent numbers by appending symbols from largest to smallest value. Standard symbols handle main values ($M=1000, D=500, C=100$, etc.), while values starting with 4 or 9 use subtractive pairs (e.g., $4 = IV$ or $900 = CM$). Listing all 13 possible Roman building blocks (including subtractive cases) in descending order allows a greedy approach: iterate through the values from highest to lowest, repeatedly subtracting the value and appending its symbol until the remaining number drops below that value.

### Algorithm
1. Start
2. Define two parallel lists sorted in descending order:
   * `values = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1]`
   * `symbols = ["M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"]`
3. Initialize an empty list `result = []` to store output components.
4. Iterate through each element in `values` using an index `i`:
   * While `num >= values[i]`:
     * Append `symbols[i]` to `result`.
     * Subtract `values[i]` from `num`.
5. Join `result` into a single string and return it.
6. Stop
