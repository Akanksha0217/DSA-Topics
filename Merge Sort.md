# 🔹 Merge Sort

## 🔹 What is Merge Sort?

Merge Sort is a **Divide and Conquer** algorithm.

👉 Divide array into smaller parts
👉 Sort each part
👉 Merge them back in sorted order

---

## 🔹 Main Idea

```text id="j0vnrf"
Divide → Sort → Merge
```

---

## 🔹 Example

Input:

```text id="v1h8s4"
[5, 2, 4, 1]
```

---

## Step 1: Divide

Split into halves:

```text id="e8gk1z"
[5, 2]   [4, 1]
```

Split again:

```text id="4iv8x5"
[5] [2] [4] [1]
```

---

## Step 2: Merge Sorted Parts

Merge:

```text id="vb2l8m"
[5] [2] → [2,5]
```

Merge:

```text id="j4rx0q"
[4] [1] → [1,4]
```

Now merge both:

```text id="wzqf2g"
[2,5] [1,4] → [1,2,4,5]
```

---

## Final Output

```text id="h7s2cy"
[1,2,4,5]
```

---

## 🔹 Visualization

```text id="5t9h6w"
[5,2,4,1]
   /   \
[5,2] [4,1]
 / \   / \
5  2  4  1
```

Merge back:

```text id="r3ku2x"
[2,5] [1,4]
   ↓
[1,2,4,5]
```

---

## 🔹 Code Implementation

```python id="h1alvl"
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        
        left = arr[:mid]
        right = arr[mid:]
        
        merge_sort(left)
        merge_sort(right)

        i = j = k = 0

        while i < len(left) and j < len(right):
            if left[i] < right[j]:
                arr[k] = left[i]
                i += 1
            else:
                arr[k] = right[j]
                j += 1
            k += 1

        while i < len(left):
            arr[k] = left[i]
            i += 1
            k += 1

        while j < len(right):
            arr[k] = right[j]
            j += 1
            k += 1
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

O(n\log n)

---

## 🔹 Why O(n log n)?

* Divide array → log n levels
* Merge each level → n work

Total:

n \times \log n

---

## 🔹 Space Complexity

O(n)

👉 Extra arrays needed

---

## 🔹 Advantages

✔ Fast
✔ Stable sorting
✔ Guaranteed O(n log n)

---

## 🔹 Disadvantages

❌ Uses extra memory

---

## 🔹 When to Use?

✔ Large datasets
✔ Stable sorting needed

---

## 🔹 Merge Sort vs Insertion Sort

| Feature    | Insertion | Merge      |
| ---------- | --------- | ---------- |
| Speed      | Slow      | Fast       |
| Best Case  | O(n)      | O(n log n) |
| Large Data | Bad       | Good       |

---

## 🔹 Common Mistakes

❌ Forgetting merge logic
❌ Wrong indices
❌ Confusing recursion flow


