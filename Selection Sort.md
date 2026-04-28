## 🔹 What is Selection Sort?

Selection Sort is a sorting algorithm where we:
👉 Repeatedly **find the minimum element**
👉 Place it at the **correct position**

---

## 🔹 How It Works

Example:

```python id="r8g5k1"
arr = [64, 25, 12, 22, 11]
```

---

### 🔸 Pass 1:

Find minimum → **11**
Swap with first element

```text id="c0y2k9"
[11, 25, 12, 22, 64]
```

---

### 🔸 Pass 2:

Find minimum from remaining → **12**

```text id="k5v8g3"
[11, 12, 25, 22, 64]
```

---

### 🔸 Pass 3:

Find minimum → **22**

```text id="j4h7l2"
[11, 12, 22, 25, 64]
```

---

### 🔸 Pass 4:

Already sorted

---

## 🔹 Final Output

```text id="u1n9b6"
[11, 12, 22, 25, 64]
```

---

## 🔹 Code Implementation

```python id="7m4xpa"
def selection_sort(arr):
    n = len(arr)

    for i in range(n):
        min_idx = i

        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j

        arr[i], arr[min_idx] = arr[min_idx], arr[i]
```

---

## 🔹 Time Complexity

* Best Case: O(n²)
* Average Case: O(n²)
* Worst Case: O(n²)

👉 Always same (no optimization)

---

## 🔹 Space Complexity

* O(1) (in-place)

---

## 🔹 Key Points

✔ Finds minimum element each time
✔ Places it in correct position
✔ Number of swaps = minimal

---

## 🔹 Advantages

✔ Simple logic
✔ Fewer swaps than bubble sort

---

## 🔹 Disadvantages

❌ Slow for large data
❌ No improvement in best case

---

## 🔹 Bubble Sort vs Selection Sort

| Feature   | Bubble Sort | Selection Sort |
| --------- | ----------- | -------------- |
| Swaps     | Many        | Fewer          |
| Speed     | Slow        | Slow           |
| Best Case | O(n)        | O(n²)          |

---

## 🔹 When to Use?

✔ Small datasets
✔ When minimizing swaps is important

---

## 🔹 Common Mistakes

❌ Not updating min index
❌ Incorrect swap
❌ Loop boundary errors

