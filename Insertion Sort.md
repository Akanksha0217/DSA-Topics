# 🔹 Insertion Sort 

## 🔹 What is Insertion Sort?

Insertion Sort builds the sorted array **one element at a time**.

👉 Pick one element
👉 Place it in its correct position in sorted part

Just like arranging playing cards in your hand 🃏

---

## 🔹 Example

```python id="3fkxut"
arr = [5, 2, 4, 6, 1]
```

---

### Pass 1:

Take **2**

Compare with 5

```text id="xbof6z"
[2, 5, 4, 6, 1]
```

---

### Pass 2:

Take **4**

Compare with 5

```text id="8p9z73"
[2, 4, 5, 6, 1]
```

---

### Pass 3:

Take **6**

Already correct

```text id="zvryb8"
[2, 4, 5, 6, 1]
```

---

### Pass 4:

Take **1**

Shift all greater elements

```text id="gpn7wq"
[1, 2, 4, 5, 6]
```

---

## 🔹 Final Output

```text id="cbg39v"
[1, 2, 4, 5, 6]
```

---

## 🔹 Code Implementation

```python id="0lbv39"
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1

        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1

        arr[j + 1] = key
```

---

## 🔹 How It Works

* Left side = sorted part
* Right side = unsorted part

👉 Insert current element in correct place

---

## 🔹 Time Complexity

### Best Case (already sorted)

O(n)

---

### Average Case

O(n^2)

---

### Worst Case (reverse sorted)

O(n^2)

---

## 🔹 Space Complexity

O(1)

👉 In-place sorting

---

## 🔹 Advantages

✔ Simple
✔ Efficient for small data
✔ Good for nearly sorted arrays

---

## 🔹 Disadvantages

❌ Slow for large data

---

## 🔹 When to Use?

✔ Small datasets
✔ Nearly sorted arrays

---

## 🔹 Insertion vs Bubble vs Selection

| Feature    | Bubble | Selection | Insertion |
| ---------- | ------ | --------- | --------- |
| Best Case  | O(n)   | O(n²)     | O(n)      |
| Worst Case | O(n²)  | O(n²)     | O(n²)     |
| Practical  | Low    | Low       | Better    |

---

## 🔹 Common Mistakes

❌ Forgetting shifting logic
❌ Wrong insertion position
❌ Loop condition errors

---

