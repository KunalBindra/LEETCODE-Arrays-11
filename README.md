# LEETCODE-Arrays-11
Let’s do a **dry run** of the **two-pointer approach**.

---

### Problem recap:

We are given an array `height[]` representing vertical lines.
We need to find two lines that form a container holding the **most water**.
Area = `min(height[i], height[j]) * (j - i)`.

---

### Example Input

```text
height = [1, 8, 6, 2, 5, 4, 8, 3, 7]
```

---

### Dry Run (Two Pointers)

**Step 1:**
Initialize:

* `left = 0` (value = 1)
* `right = 8` (value = 7)
* `maxArea = 0`

**Step 2:**
Compute area = `min(1, 7) * (8 - 0) = 1 * 8 = 8`
→ `maxArea = 8`
Move **left++** (since 1 < 7).

---

**Step 3:**
`left = 1` (value = 8), `right = 8` (value = 7)
Area = `min(8, 7) * (8 - 1) = 7 * 7 = 49`
→ `maxArea = 49`
Move **right--** (since 7 < 8).

---

**Step 4:**
`left = 1` (value = 8), `right = 7` (value = 3)
Area = `min(8, 3) * (7 - 1) = 3 * 6 = 18`
→ `maxArea = 49` (no change)
Move **right--** (since 3 < 8).

---

**Step 5:**
`left = 1` (value = 8), `right = 6` (value = 8)
Area = `min(8, 8) * (6 - 1) = 8 * 5 = 40`
→ `maxArea = 49` (no change)
Move **right--** (equal heights → choose any).

---

**Step 6:**
`left = 1` (value = 8), `right = 5` (value = 4)
Area = `min(8, 4) * (5 - 1) = 4 * 4 = 16`
→ `maxArea = 49`
Move **right--**.

---

**Step 7:**
`left = 1` (value = 8), `right = 4` (value = 5)
Area = `min(8, 5) * (4 - 1) = 5 * 3 = 15`
→ `maxArea = 49`
Move **right--**.

---

**Step 8:**
`left = 1` (value = 8), `right = 3` (value = 2)
Area = `min(8, 2) * (3 - 1) = 2 * 2 = 4`
→ `maxArea = 49`
Move **right--**.

---

**Step 9:**
`left = 1` (value = 8), `right = 2` (value = 6)
Area = `min(8, 6) * (2 - 1) = 6 * 1 = 6`
→ `maxArea = 49`
Move **right--**.

---

Now `left == right`, stop.

---

### Final Answer:

`maxArea = 49`

---
