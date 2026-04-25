# 🔍 Binary Search 

## 🔹 What is Binary Search?

Binary Search is an efficient algorithm used to find an element in a **sorted array** by repeatedly dividing the search space into half.

👉 Key Idea:
Instead of checking every element (like Linear Search), we **eliminate half of the data each step**

---

## 🔹 Prerequisite

✅ Array must be **sorted**

❌ If not sorted → Binary Search will NOT work

---

## 🔹 How Binary Search Works

Example:

```
arr = [10, 20, 30, 40, 50]
target = 30
```

### Steps:

1. Find middle element
   mid = (left + right) // 2

2. Compare:

   * If arr[mid] == target → Found
   * If arr[mid] < target → Search right half
   * If arr[mid] > target → Search left half

---

## 🔹 Code (Iterative)

```python
def binary_search(arr, target):
    left = 0
    right = len(arr) - 1

    while left <= right:
        mid = (left + right) // 2

        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1

    return -1
```

---

## 🔹 Code (Recursive)

```python
def binary_search(arr, left, right, target):
    if left > right:
        return -1

    mid = (left + right) // 2

    if arr[mid] == target:
        return mid
    elif arr[mid] < target:
        return binary_search(arr, mid + 1, right, target)
    else:
        return binary_search(arr, left, mid - 1, target)
```

---

## 🔹 Time Complexity

* Best Case: O(1)
* Worst Case: O(log n)
* Average Case: O(log n)

👉 Very fast compared to O(n)

---

## 🔹 Why O(log n)?

Because each step reduces the problem size:

```
n → n/2 → n/4 → n/8 → ...
```

---

## 🔹 Space Complexity

* Iterative: O(1)
* Recursive: O(log n) (due to recursion stack)

---

## 🔹 Important Variations (Interview 🔥)

### 1. First Occurrence

Find first position of target in sorted array

### 2. Last Occurrence

Find last position

### 3. Lower Bound

First element ≥ target

### 4. Upper Bound

First element > target

### 5. Search in Rotated Sorted Array

---

## 🔹 Common Mistakes

❌ Using binary search on unsorted array
❌ Infinite loop (wrong condition)
❌ Incorrect mid calculation

👉 Safe mid formula:

```
mid = left + (right - left) // 2
```

---

## 🔹 When to Use Binary Search

✔ Sorted array
✔ Large dataset
✔ Need fast search

---

## 🔹 When NOT to Use

❌ Unsorted data
❌ Small input (linear is fine)

---

## 🔹 Real-Life Example

👉 Searching a word in dictionary
👉 Guessing number game (high/low)

---

## 🔹 Quick Comparison

| Feature     | Linear Search | Binary Search  |
| ----------- | ------------- | -------------- |
| Requirement | No sorting    | Must be sorted |
| Time        | O(n)          | O(log n)       |
| Speed       | Slow          | Fast           |

---

## 🔹 Practice Questions

1. Implement binary search
2. Find first & last occurrence
3. Count occurrences of element
4. Search in rotated sorted array

---

## 🔹 Final Summary

* Works only on sorted arrays
* Divides search space in half
* Time complexity = O(log n)
* Very important for interviews

---
