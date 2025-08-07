# 📘 DSA Journey Catalog

Welcome to my **DSA (Data Structures and Algorithms)** journey! This repository is a personal log of the concepts I’ve learned, problems I’ve solved, and progress I’ve made while mastering DSA. It serves both as a revision notebook and a motivation tracker.

---

## 🗓️ Progress Tracker

---

### 📅 Day 1
- **Topics Covered:**
  - Binary Search
  - Pivot in Array

#### 1. [Find Peak in a Mountain Array](https://leetcode.com/problems/peak-index-in-a-mountain-array/)
- ✅ **Approach:** Binary search for `arr[mid] < arr[mid+1]` to locate the increasing slope end.
- 💡 **Method Used:** `peakIndexInMountainArray(vector<int>& arr)`
- 💻 **C++ Snippet:**
  ```cpp
  while (low < high) {
      int mid = low + (high - low) / 2;
      if (arr[mid] < arr[mid + 1]) low = mid + 1;
      else high = mid;
  }
  return low;
2. Find First and Last Occurrence
✅ Approach: Modified binary search twice to find leftmost and rightmost index.

💡 Method Used: Binary search (2 passes)

💻 C++ Snippet:

cpp
Copy code
int left = findBound(nums, target, true);
int right = findBound(nums, target, false);
📅 Day 2
Topics Covered:

Binary Search Applications

1. Search in Rotated Sorted Array
✅ Approach: Modified binary search using inflection point logic.

💡 Key Idea: Determine which half is sorted and reduce search space accordingly.

2. Square Root using Binary Search
✅ Approach: Binary search between 0 and x to find integer square root.

💻 C++ Snippet:

cpp
Copy code
while (low <= high) {
    long mid = (low + high) / 2;
    if (mid * mid <= x) {
        ans = mid;
        low = mid + 1;
    } else high = mid - 1;
}
📅 Day 3
Topics Covered:

Strings

String Arrays

1. Valid Palindrome
✅ Approach: Two-pointer technique ignoring non-alphanumerics.

💡 Method Used: isalnum() with lowercased comparison.

2. Reverse Words in a String
✅ Approach: Trim spaces, split by space, reverse the array.

💻 Python Snippet:

python
Copy code
return " ".join(reversed(s.strip().split()))
📅 Day 4
Topics Covered:

Strings

Sliding Window

1. Implement strStr()
✅ Approach: Brute-force substring match.

2. Permutation in String
✅ Approach: Sliding window with frequency arrays.

3. String Compression
✅ Approach: Two-pointer write-while-read technique.

📅 Day 5
Topics Covered:

2D Arrays

1. Wave Print (Custom Problem)
✅ Approach: Alternate up-down column traversal.

2. Spiral Print (Custom Problem)
✅ Approach: Layer-wise clockwise traversal using boundaries.

📅 Day 6
Topics Covered:

2D Arrays

1. Search a 2D Matrix
✅ Approach: Binary search on virtual 1D array.

2. Search a 2D Matrix II
✅ Approach: Start from top-right, move left/down.

📅 Day 7
Topic Covered:

Recursion

1. Sort Stack Using Recursion
✅ Approach: Remove top, sort rest, insert sorted.

📅 Day 8
Topic Covered:

Recursion

1. Binary Search (Recursive)
✅ Approach: Classic recursion with mid, low, high.

📅 Day 9
Topic Covered:

Recursion

1. Subsets
✅ Approach: Backtracking by include/exclude current element.

2. Subsets II
✅ Approach: Similar to Subsets I but skip duplicates using sorting.

📅 Day 10
Topic Covered:

Recursion

1. Phone Number Letter Combinations
✅ Approach: Backtracking with digit-to-char mapping.

📅 Day 11
Topic Covered:

Linked List

1. Reverse Linked List
✅ Approach: Iterative pointer reversal using prev, curr.

🎯 Goal
To build a strong foundation in core DSA concepts and solve a wide range of problems with increasing difficulty, preparing for technical interviews and competitive programming.

🛠️ Tools Used
Language: Python / C++

Platforms: LeetCode, Codeforces, GeeksforGeeks

Version Control: Git + GitHub

🚀 How to Use
Feel free to explore the daily logs, code snippets, and solutions. You can fork this repository and start your own DSA journey too!

🙌 Let’s Connect!
If you're also on your DSA journey, let’s connect and grow together!

python
Copy code

---

Let me know if you'd like this as a downloadable `README.md` file or 
