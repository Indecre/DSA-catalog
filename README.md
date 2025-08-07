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
```

#### 2. [Find First and Last Occurrence](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- ✅ **Approach:** Two binary searches: one for the first and one for the last occurrence.
- 💡 **Method Used:** `searchRange(vector<int>& nums, int target)`
- 💻 **C++ Snippet:**
```cpp
int binarySearch(bool findFirst) {
    int res = -1;
    while (low <= high) {
        int mid = (low + high) / 2;
        if (nums[mid] == target) {
            res = mid;
            findFirst ? high = mid - 1 : low = mid + 1;
        }
        else if (nums[mid] < target) low = mid + 1;
        else high = mid - 1;
    }
    return res;
}
```

---

### 📅 Day 2
- **Topics Covered:**
  - Binary Search Applications

#### 1. [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- ✅ **Approach:** Modified binary search using pivot logic.
- 💡 **Method Used:** `search(vector<int>& nums, int target)`

#### 2. [Square Root using Binary Search](https://leetcode.com/problems/sqrtx/)
- ✅ **Approach:** Binary search between 1 and x/2, compare mid*mid.
- 💡 **Method Used:** `mySqrt(int x)`

---

### 📅 Day 3
- **Topics Covered:**
  - Strings
  - String Arrays

#### 1. [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
- ✅ **Approach:** Two pointers from both ends, skip non-alphanumerics.

#### 2. [Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
- ✅ **Approach:** Trim + reverse each word + reverse entire string.

---

### 📅 Day 4
- **Topics Covered:**
  - Strings
  - Sliding Window

#### 1. [Implement strStr()](https://leetcode.com/problems/implement-strstr/)
- ✅ **Approach:** Sliding window to compare substring matches.

#### 2. [Permutation in String](https://leetcode.com/problems/permutation-in-string/)
- ✅ **Approach:** Compare frequency maps of sliding window and target.

#### 3. [String Compression](https://leetcode.com/problems/string-compression/)
- ✅ **Approach:** Use two pointers to modify array in-place.

---

### 📅 Day 5
- **Topics Covered:**
  - 2D Arrays

#### 1. Wave Print of a 2D Matrix
- ✅ **Approach:** Traverse columns alternatively top to bottom and bottom to top.

#### 2. Spiral Print of a 2D Matrix
- ✅ **Approach:** Maintain 4 boundaries and iterate in spiral fashion.

---

### 📅 Day 6
- **Topics Covered:**
  - 2D Arrays

#### 1. [Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)
- ✅ **Approach:** Flatten the matrix logically and apply binary search.

#### 2. [Search a 2D Matrix II](https://leetcode.com/problems/search-a-2d-matrix-ii/)
- ✅ **Approach:** Start from top-right, eliminate row or column based on comparison.

---

### 📅 Day 7
- **Topics Covered:**
  - Recursion

#### 1. [Sort an Array Using Recursion](https://www.geeksforgeeks.org/sort-a-stack-using-recursion/)
- ✅ **Approach:** Pop elements recursively and insert them back in sorted order.
- 💻 **C++ Snippet:**
```cpp
void insert(vector<int>& arr, int temp) {
    if (arr.empty() || arr.back() <= temp) {
        arr.push_back(temp);
        return;
    }
    int val = arr.back(); arr.pop_back();
    insert(arr, temp);
    arr.push_back(val);
}
```

---

### 📅 Day 8
- **Topics Covered:**
  - Recursion

#### 1. [Binary Search (Recursive)](https://leetcode.com/problems/binary-search/)
- ✅ **Approach:** Base case and recursive reduction of search space.

---

### 📅 Day 9
- **Topics Covered:**
  - Recursion

#### 1. [Subsets](https://leetcode.com/problems/subsets/)
- ✅ **Approach:** Backtracking to include/exclude elements.

#### 2. [Subsets II](https://leetcode.com/problems/subsets-ii/)
- ✅ **Approach:** Same as Subsets but skip duplicates using sorted array.

---

### 📅 Day 10
- **Topics Covered:**
  - Recursion

#### 1. [Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
- ✅ **Approach:** Map each digit to possible characters and recurse to build combinations.
- 💻 **C++ Snippet:**
```cpp
void backtrack(string& digits, int index, string& path, vector<string>& res, vector<string>& map) {
    if (index == digits.size()) {
        res.push_back(path);
        return;
    }
    for (char c : map[digits[index] - '0']) {
        path.push_back(c);
        backtrack(digits, index + 1, path, res, map);
        path.pop_back();
    }
}
```

---

### 📅 Day 11
- **Topics Covered:**
  - Linked List

#### 1. [Reverse a Linked List](https://leetcode.com/problems/reverse-linked-list/)
- ✅ **Approach:** Iteratively reverse the pointers using three variables.
- 💻 **C++ Snippet:**
```cpp
ListNode* reverseList(ListNode* head) {
    ListNode* prev = nullptr;
    while (head) {
        ListNode* next = head->next;
        head->next = prev;
        prev = head;
        head = next;
    }
    return prev;
}
```

---

## 🎯 Goal
To build a strong foundation in core DSA concepts and solve a wide range of problems with increasing difficulty, preparing for technical interviews and competitive programming.

---

## 🛠️ Tools Used
- Language: Python / C++
- Platform: [LeetCode](https://leetcode.com/), [Codeforces](https://codeforces.com/), [GeeksforGeeks](https://www.geeksforgeeks.org/)
- Version Control: Git + GitHub

---

## 🚀 How to Use
Feel free to explore the daily logs, code snippets, and approaches. You can fork this repository and start your own DSA journey too!

---

## 🙌 Let’s Connect!
If you're also on your DSA journey, let’s connect and grow together!
