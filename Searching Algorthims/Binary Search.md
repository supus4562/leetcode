# Pattern: Binary Search

##  Core Concept
If you have a sorted use Binary Search to find any element if that exists in the array. It divides the array in half and since the array is sorted it checks whether the  element should exist in right half or left half and after deciding this it discards the remaining half. Conserving compute time. 

##  When to Use (Triggers)
- Find an element in a sorted array
- Fasted searching algorthm on a sorted ds
- Constraint `O(log n)`

##  The Skeleton Code
Recursive approach:
```cpp
template<typename C>
int binSearch(C arr[], C target, int start, int end) {
    // Base case: target not found
    if (start > end) {
        return -1;
    }

    // Calculate middle safely to avoid integer overflow
    int middle = start + (end - start) / 2;

    // Target found
    if (arr[middle] == target) {
        return middle;
    }
    
    // Target is in the left half
    if (arr[middle] > target) {
        return binSearch(arr, target, start, middle - 1);
    }
    
    // Target is in the right half
    return binSearch(arr, target, middle + 1, end);
}
```

##  Problems
1. [33. Search in Rotated Sorted Array
](https://leetcode.com/problems/search-in-rotated-sorted-array?envType=daily-question&envId=2026-05-22)
