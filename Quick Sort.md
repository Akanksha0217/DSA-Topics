# 🔹 Quick Sort – Complete Notes (DSA)

## 🔹 What is Quick Sort?

Quick Sort is a **Divide and Conquer** sorting algorithm.

👉 Select a **pivot**
👉 Place smaller elements on left
👉 Place larger elements on right
👉 Repeat recursively

---

## 🔹 Main Idea

```text id="4zh0vb"
Pick Pivot → Partition → Recursively Sort
```

---

## 🔹 Example

Input:

```text id="mqiv7g"
[5, 2, 7, 1, 3]
```

Choose pivot:

```text id="f3r1r7"
pivot = 5
```

Partition:

```text id="uhx1el"
left = [2,1,3]
pivot = [5]
right = [7]
```

Now sort left recursively.

---

## Final Result

```text id="6sr3t7"
[1,2,3,5,7]
```

---

## 🔹 Visualization

```text id="j3ukvh"
[5,2,7,1,3]
   pivot=5
```

Split:

```text id="c4l0t7"
[2,1,3] 5 [7]
```

Sort left:

```text id="cuh5ki"
[1,2,3]
```

Final:

```text id="q7m4kz"
[1,2,3,5,7]
```

---

## 🔹 Code Implementation (Simple Version)

```python id="1xzk0z"
def quick_sort(arr):
    if len(arr) <= 1:
        return arr

    pivot = arr[len(arr)//2]

    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]

    return quick_sort(left) + middle + quick_sort(right)
```

---

## 🔹 How Code Works

### Base Case

```python id="7oow2r"
if len(arr) <= 1:
    return arr
```

👉 Single element is already sorted

---

### Choose Pivot

```python id="3zwit8"
pivot = arr[len(arr)//2]
```

---

### Partition

```python id="g69q1q"
left = [x for x in arr if x < pivot]
right = [x for x in arr if x > pivot]
```

---

### Recursive Sort

```python id="w6pl3m"
return quick_sort(left) + middle + quick_sort(right)
```

---

## 🔹 Time Complexity

### Best Case

O(n\log n)

---

### Average Case

O(n\log n)

---

### Worst Case

O(n^2)

Worst happens when pivot is poor
Example:

```text id="44fz2v"
[1,2,3,4,5]
```

---

## 🔹 Space Complexity

O(\log n)

---

## 🔹 Why Quick Sort is Fast?

Because:

* Partitioning is efficient
* Usually divides array well

---

## 🔹 Advantages

✔ Fast in practice
✔ Good cache performance
✔ Widely used

---

## 🔹 Disadvantages

❌ Worst case O(n²)
❌ Not stable

---

## 🔹 Merge Sort vs Quick Sort

| Feature | Merge Sort | Quick Sort |
| ------- | ---------- | ---------- |
| Best    | O(n log n) | O(n log n) |
| Worst   | O(n log n) | O(n²)      |
| Space   | O(n)       | O(log n)   |

---

## 🔹 When to Use?

✔ Fast practical sorting
✔ Large datasets

---

## 🔹 Common Mistakes

❌ Bad pivot choice
❌ Infinite recursion
❌ Wrong partition logic

---


