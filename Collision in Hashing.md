# 🔹 Collision in Hashing – Complete Explanation

## 🔹 What is Collision?

👉 Collision happens when:
Two different keys map to the **same index** in a hash table

---

## 🔹 Example

Suppose hash function:

```text
index = key % 5
```

Keys:

```text
10 % 5 = 0
15 % 5 = 0
```

👉 Both go to index 0 → **Collision occurs**

---

# 🔥 How to Handle Collisions?

There are **2 main techniques**:

---

# 🔹 1. Chaining (Most Common)

## ✅ Idea

👉 Store multiple values at same index using a **list (chain)**

---

## 🔹 Visualization

```text
Index | Values
0     | [10 → 15 → 20]
1     | [6]
2     | []
```

---

## 🔹 Python Example

```python
hash_table = [[] for _ in range(5)]

def insert(key):
    index = key % 5
    hash_table[index].append(key)

insert(10)
insert(15)

print(hash_table)
```

---

## ⏱️ Complexity

* Average: O(1)
* Worst: O(n) (if all go to same index)

---

## ✅ Advantages

✔ Easy to implement
✔ Handles many collisions well

---

## ❌ Disadvantages

❌ Uses extra memory (lists)

---

# 🔹 2. Open Addressing

## ✅ Idea

👉 If collision occurs, **find another empty slot**

---

## 🔹 Types of Open Addressing

---

### 🔸 1. Linear Probing

👉 Move to next index

```text
index = (index + 1) % size
```

---

## 🔹 Example

```text
Insert 10 → index 0  
Insert 15 → index 0 (collision)  
Try index 1 → place there
```

---

### 🔸 2. Quadratic Probing

👉 Jump using square pattern

```text
index = (index + i²) % size
```

---

### 🔸 3. Double Hashing

👉 Use another hash function

```text
index = (h1(key) + i * h2(key)) % size
```

---

## ⏱️ Complexity

* Average: O(1)
* Worst: O(n)

---

## ✅ Advantages

✔ No extra memory needed

---

## ❌ Disadvantages

❌ More complex
❌ Clustering problem (linear probing)

---

# 🔥 Chaining vs Open Addressing

| Feature        | Chaining           | Open Addressing |
| -------------- | ------------------ | --------------- |
| Storage        | List at each index | Single array    |
| Memory         | More               | Less            |
| Implementation | Easy               | Complex         |
| Performance    | Stable             | Can degrade     |

---


# 🚀 Quick Summary

* Collision = same index for different keys
* Chaining → store multiple values
* Open Addressing → find new position

---
