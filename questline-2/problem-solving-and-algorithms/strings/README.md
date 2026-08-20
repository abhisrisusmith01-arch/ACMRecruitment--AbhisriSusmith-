# Problem Solving & Algorithms - Strings🧵

## Problem 1: Valid Palindrome

### Thought Process & Approach
A phrase is a palindrome if it reads the same forward and backward after removing all non-alphanumeric characters and converting all letters to lowercase.

The approach filters out invalid characters and converts the valid characters to lowercase in a single pass. The resulting cleaned string is then compared directly against its reverse.

### Algorithm
START
1. Filter the input string `s` using a generator expression: retain only alphanumeric characters (`char.isalnum()`) converted to lowercase (`char.lower()`).
2. Join the filtered characters into a new string `new_s`.
3. Generate the reversed string using Python slicing: `new_s[::-1]`.
4. Return `True` if `new_s == new_s[::-1]`, otherwise return `False`.
STOP

## Problem 2: Zigzag Conversion

### Thought Process & Approach
The string `s` is written in a zigzag pattern across `numRows` and read line-by-line.

Instead of creating a full 2D grid matrix, we simulate the bounce movement across row "buckets":
* Maintain an array of strings representing each row.
* Walk through the string while keeping track of `curr_row` and `direction`.
* Reverse direction whenever hitting boundary rows (`row 0` or `row numRows - 1`).

### Algorithm
START
1. **Base Case:** If `numRows == 1` or `numRows >= len(s)`, return `s` directly since no zigzag conversion is needed.
2. Initialize an array of strings `rows = [""] * numRows`, set `curr_row = 0`, and set `direction = -1`.
3. Iterate through each character `char` in string `s`:
   * Append `char` to `rows[curr_row]`.
   * If `curr_row == 0` or `curr_row == numRows - 1`, flip direction: `direction = -direction`.
   * Move to the next row: `curr_row += direction`.
4. Concatenate all rows into a single string using `"".join(rows)` and return.
STOP
