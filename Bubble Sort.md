# 🔹 Bubble Sort

## 🔹 What is Bubble Sort?

Bubble Sort is a simple sorting algorithm where we:
👉 Compare **adjacent elements**
👉 Swap them if they are in the wrong order

After each pass, the **largest element “bubbles” to the end**

---

## 🔹 Example

```python
arr = [5, 3, 8, 4]
```

### Pass 1:

* Compare 5 & 3 → swap → [3, 5, 8, 4]
* Compare 5 & 8 → no swap
* Compare 8 & 4 → swap → [3, 5, 4, 8]

👉 Largest (8) is now at correct position

---

### Pass 2:

* Compare 3 & 5 → no swap
* Compare 5 & 4 → swap → [3, 4, 5, 8]

---

### Pass 3:

* Compare 3 & 4 → no swap

👉 Sorted array: [3, 4, 5, 8]

---

## 🔹 Basic Code

```python
def bubble_sort(arr):
    n = len(arr)
    
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```

---

## 🔹 Optimized Code (Important 🔥)

👉 Stop early if array is already sorted

```python
def bubble_sort(arr):
    n = len(arr)
    
    for i in range(n):
        swapped = False
        
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        
        if not swapped:
            break
```

---

## 🔹 Time Complexity

* Worst Case: O(n²)
* Average Case: O(n²)
* Best Case: O(n) (optimized version)

---

## 🔹 Space Complexity

* O(1) (in-place sorting)

---

## 🔹 Key Points

✔ Simple and easy to understand
✔ Works by swapping adjacent elements
✔ Largest element moves to end each pass

---

## 🔹 When to Use?

✔ Small datasets
✔ Educational purpose (learning sorting)

---

## 🔹 Common Mistakes

❌ Forgetting `n-i-1` in loop
❌ Not optimizing with `swapped` flag
❌ Running unnecessary passes

---

---
