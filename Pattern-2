# 🟢 Sliding Window Pattern – Concept, Types, Templates & Practice

---

## 📌 What is the Sliding Window Pattern?

The **Sliding Window** pattern is used to efficiently process **continuous subarrays or substrings** by maintaining a moving window over the data.

🎯 **Primary Goal:**  
Reduce time complexity from **O(n²)** to **O(n)** by avoiding repeated computations.

---

## 📌 Why Sliding Window Exists

### ❌ Brute Force Approach
Check all possible subarrays / substrings

- Generates O(n²) windows
- Each window may take O(n) to evaluate
- ❌ Total complexity: O(n³) or O(n²)

---

### ✅ Optimized Sliding Window Approach
Reuse previous window work
Expand and shrink window intelligently

- Traverse data only once
- Maintain window state dynamically
- ✅ Total complexity: O(n)

---

## 📌 When to Identify Sliding Window in Interviews

### 🔑 Trigger Keywords
If the problem contains:
- subarray
- substring
- continuous
- longest / shortest
- maximum / minimum
- at most / at least k

👉 **Think Sliding Window immediately**

---

## 📌 Types of Sliding Window Patterns

There are **two major types** of sliding window problems.

---

# 1️⃣ Fixed Size Sliding Window

---

## 📌 What is Fixed Size Sliding Window?

The window size is **constant (k)** throughout the traversal.

- Window size = k
- Left and right pointers move together

---

## 📌 Fixed Size Window Intuition

1. Build the first window
2. Slide the window forward:
   - Add the next element
   - Remove the previous element
3. Update the answer

---

## 📌 Fixed Size Sliding Window Template (Python)

```python
window_sum = 0
left = 0

for right in range(len(nums)):
    window_sum += nums[right]

    if right - left + 1 == k:
        # update answer
        window_sum -= nums[left]
        left += 1
```

---

## 📌 Fixed Size Sliding Window – Common Use Cases

- Maximum / minimum sum subarray of size k
- Average of subarray of size k
- First negative number in every window
- Maximum element in each window

---

## 📌 Fixed Size Sliding Window – Practice Problems

### Maximum Sum Subarray of Size K
🔗 https://leetcode.com/problems/maximum-average-subarray-i/

### Sliding Window Maximum
🔗 https://leetcode.com/problems/sliding-window-maximum/

### First Negative Number in Every Window (GFG)

### Subarray with Given Sum (Fixed Size)

### Maximum Number of Vowels in a Substring of Given Length
🔗 https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/

---

# 2️⃣ Variable Size Sliding Window

---

## 📌 What is Variable Size Sliding Window?

The window size changes dynamically based on a condition.

- Expand window → condition breaks → shrink window

---

## 📌 Variable Size Window Intuition

1. Expand the window using the right pointer
2. If condition is violated:
   - Shrink window from the left
3. Keep updating the answer when the window is valid

---

## 📌 Variable Size Sliding Window Template (Python)

```python
left = 0
window_state = {}

for right in range(len(s)):
    # include s[right] in window_state

    while condition_is_invalid:
        # remove s[left] from window_state
        left += 1

    # update answer
```

---

## 📌 Variable Size Sliding Window – Common Use Cases

- Longest substring without repeating characters
- Longest subarray with sum ≤ k
- Minimum window substring
- At most / exactly k distinct elements

---

## 📌 Variable Size Sliding Window – Practice Problems

### Longest Substring Without Repeating Characters
🔗 https://leetcode.com/problems/longest-substring-without-repeating-characters/

### Minimum Window Substring
🔗 https://leetcode.com/problems/minimum-window-substring/

### Longest Repeating Character Replacement
🔗 https://leetcode.com/problems/longest-repeating-character-replacement/

### Subarrays with K Different Integers
🔗 https://leetcode.com/problems/subarrays-with-k-different-integers/

### Longest Subarray of 1's After Deleting One Element
🔗 https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element/

---

## 🔁 Sliding Window vs Two Pointers

| Aspect | Sliding Window | Two Pointers |
|--------|---|---|
| Range | Continuous range | May not be continuous |
| Constraints | Has constraints | Often no constraints |
| Movement | Expands and shrinks | Usually simple movement |
| Applications | Subarrays / substrings | Pair problems |

---

## ⚠️ Common Interview Mistakes

1. Using nested loops instead of sliding window
2. Forgetting to shrink window when condition fails
3. Updating answer at the wrong time
4. Mixing fixed and variable window logic

---

## 🎯 One-Line Interview Explanation

"Since the problem involves finding an optimal continuous subarray under constraints, I'll use the Sliding Window pattern to achieve linear time complexity."

---

## 🚀 What's Next

**Next steps:**

1. Solve fixed size sliding window problems with brute force + optimized approach
2. Solve variable size sliding window problems with full explanation
3. Push solutions and explanations to GitHub

---

