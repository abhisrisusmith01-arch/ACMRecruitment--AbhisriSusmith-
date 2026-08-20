# Greedy Algorithms

## Problem 1: Lemonade Change🍋

### Thought Process & Approach
We simulate a lemonade stand where each lemonade costs $5. Customers pay using $5, $10, or $20 bills, and we must provide correct change sequentially.

* **$5 Bill:** No change required. Retain the bill (`five += 1`).
* **$10 Bill:** Requires $5 as change. Return one $5 bill and retain the $10 bill (`five -= 1`, `ten += 1`).
* **$20 Bill:** Requires $15 as change. We greedily prioritize returning one $10 bill and one $5 bill over three $5 bills, because $5 bills are strictly more versatile for future change.

### Algorithm
START
1. Initialize counters `five = 0` and `ten = 0`.
2. Iterate through each payment `bill` in `bills`:
   * **If `bill == 5`:** Increment `five` by 1.
   * **If `bill == 10`:** Check if `five > 0`. If true, decrement `five` by 1 and increment `ten` by 1. Otherwise, return `False`.
   * **If `bill == 20`:** 
     * First choice: If `ten > 0` and `five > 0`, decrement both `ten` and `five` by 1.
     * Fallback choice: If `five >= 3`, decrement `five` by 3.
     * Otherwise, return `False`.
3. If all transactions succeed, return `True`.
STOP
## Problem 2: Assign Cookies 🍪

### Thought Process & Approach
We want to maximize the total number of content children. Giving a large cookie to a child with a small greed factor wastes that cookie's potential to satisfy a child with a larger greed factor. 

We use a **Greedy Algorithm with Two Pointers**:
1. Sort both the children's greed array `g` and the cookie sizes array `s` in ascending order.
2. Iterate through both arrays using pointers to pair the smallest available cookie that satisfies the child with the smallest greed factor.
3. If a cookie satisfies the current child, advance to the next child. Regardless, move to the next cookie to evaluate.

### Algorithm
START
1. Sort arrays `g` and `s` in non-decreasing order.
2. Initialize pointers `child_i = 0` and `cookie_j = 0`.
3. Loop while `child_i < len(g)` and `cookie_j < len(s)`:
   * **If `s[cookie_j] >= g[child_i]`:** The current cookie satisfies the child, so increment `child_i` by 1.
   * Increment `cookie_j` by 1 to inspect the next cookie.
4. Return `child_i` (representing the total number of satisfied children).
STOP
