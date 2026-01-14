# 🟢 Pattern 1: Array & Hashing – Deep Mode

## 📌 What is the Array & Hashing Pattern?

**Array & Hashing** is a fundamental DSA pattern focused on:
- Traversing arrays efficiently
- Storing and retrieving information in constant time
- Eliminating unnecessary nested loops

🎯 **Primary Goal:**  
Reduce time complexity from **O(n²)** to **O(n)** by using hashing.

---

## 📌 Why This Pattern Exists

### ❌ Brute Force Thinking
For each element:
Check all other elements
- Time Complexity: O(n²)
- Not acceptable in interviews

### ✅ Optimized Thinking
Traverse once
Store useful information
Reuse it in O(1) time

This optimization is achieved using **hashing**.

---

## 📌 Python Tools Used in This Pattern

| Tool | Usage |
|----|----|
| `dict` | Frequency counting, index mapping |
| `set` | Duplicate detection, visited tracking |
| `defaultdict` | Cleaner frequency logic |
| `Counter` | Quick frequency calculation |
| `list` | Direct index access |

📌 **Python dictionaries and sets provide O(1) average lookup time**, making them ideal for interviews.

---

## 📌 When to Identify Array & Hashing in Interviews

### 🔑 Common Trigger Keywords
If the problem mentions:
- count
- frequency
- duplicate
- exists
- pair
- subarray
- longest / shortest
- seen before

👉 **Think: Array + Hashing first**

---

## 📌 Internal Sub-Patterns

Array & Hashing consists of multiple internal patterns:

1. Frequency Counting  
2. Seen / Visited Set  
3. Index Mapping  
4. Prefix Sum  
5. Running Sum  
6. Difference Array (advanced)

Each sub-pattern is studied independently and deeply.

---

## 🔹 Sub-Pattern 1: Frequency Counting

### 📌 Concept
Frequency counting tracks how many times each element appears.

**Example:**
Input: [1, 2, 2, 3, 3, 3]
Output:
{
1: 1,
2: 2,
3: 3
}

---

### 📌 When to Use
- Count occurrences
- Find most frequent element
- Top-K frequency problems
- Anagram checks

---

### 📌 Python Template

```python
freq = {}
for num in nums:
    if num in freq:
        freq[num] += 1
    else:
        freq[num] = 1

Cleaner approach:
from collections import defaultdict

freq = defaultdict(int)
for num in nums:
    freq[num] += 1

## **📌 Interview Explanation**

“I’m using a hashmap to count frequencies in one pass, reducing time complexity to O(n).”
## **🔹 Sub-Pattern 2: Seen / Visited Set
**
## 📌 Concept

Track elements already encountered.

Example:
Input: [1, 2, 3, 1]
Duplicate found: 1
## **📌 When to Use**

Detect duplicates

Check repeated elements

Membership validation
## **📌 Python Template**

seen = set()
for num in nums:
    if num in seen:
        return True
    seen.add(num)
return False

📌 Interview Explanation

“Using a set gives constant-time lookup, allowing duplicate detection in one traversal.”
🔹 Sub-Pattern 3: Index Mapping
📌 Concept

Map values to their indices.

Example:
nums = [2, 7, 11, 15]
index_map = {
  2: 0,
  7: 1,
  11: 2,
  15: 3
}
📌 When to Use

Pair problems (e.g., Two Sum)

Index-based lookups
📌 Python Template
index_map = {}
for i, num in enumerate(nums):
    if target - num in index_map:
        return [index_map[target - num], i]
    index_map[num] = i

📌 Interview Explanation

“I store value-to-index mapping to find complements in constant time.”

🔹 Sub-Pattern 4: Prefix Sum
📌 Concept

Prefix sum stores cumulative sums.

Example:
nums = [1, 2, 3]
prefix = [1, 3, 6]
📌 Why Prefix Sum Is Powerful

Subarray sum problems

Range queries

Count subarrays with given sum

📌 Python Template
prefix_sum = 0
count = 0
seen = {0: 1}

for num in nums:
    prefix_sum += num
    if prefix_sum - k in seen:
        count += seen[prefix_sum - k]
    seen[prefix_sum] = seen.get(prefix_sum, 0) + 1

📌 Interview Explanation

“Prefix sums help compute subarray sums in constant time.”

⚠️ Common Interview Mistakes

Forgetting {0:1} in prefix sum problems

Updating hashmap before checking condition

Using nested loops instead of hashing

Ignoring edge cases (empty array, single element)

🚀 What’s Next

Next step in this pattern:

LeetCode Practice

5 problems per sub-pattern

Python solutions + explanations

Interview-style reasoning

👉 Next file will start with:
Frequency Counting – 5 LeetCode Problems

📌 This document is part of a structured, pattern-based DSA interview preparation approach.


---

## ✅ Next Action
1️⃣ Create the file  
2️⃣ Push to GitHub  
3️⃣ Commit message example:


Added Array & Hashing deep mode concepts and templates


When ready, say:
> **“Start Frequency Counting problems”**

We’ll move to **real interview problems next** 💪🔥




