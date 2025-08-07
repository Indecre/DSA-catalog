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
- ✅ **Approach:** Binary search for arr[mid] < arr[mid+1] to locate the increasing slope end.
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
