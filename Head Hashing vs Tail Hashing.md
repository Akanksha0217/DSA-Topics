# 🔹 Head Hashing vs Tail Hashing (in Chaining)

## 🔹 Context

👉 When using **chaining**, each index stores multiple elements using a **linked list**

Now question is:
👉 When inserting a new element, where do we add it?

* At the **start (head)** → Head Hashing
* At the **end (tail)** → Tail Hashing

---

# 🔹 1. Head Hashing

## ✅ Idea

👉 Insert new element at the **beginning** of the list

---

## 🔹 Visualization

Insert: 10 → 15 → 20

```text id="m2f7tq"
Index 0:
[20 → 15 → 10]
```

👉 Latest element comes first

---

## 🔹 Code (Concept)

```python id="8z3d0m"
node.next = head
head = node
```

---

## ⏱️ Time Complexity

👉 O(1) (very fast)

---

## ✅ Advantages

✔ Fast insertion
✔ No traversal needed

---

## ❌ Disadvantages

❌ Order gets reversed
❌ Searching may be slightly confusing

---

# 🔹 2. Tail Hashing

## ✅ Idea

👉 Insert new element at the **end** of the list

---

## 🔹 Visualization

Insert: 10 → 15 → 20

```text id="4n0r3k"
Index 0:
[10 → 15 → 20]
```

👉 Order is maintained

---

## 🔹 Code (Concept)

```python id="5dklc0"
temp = head
while temp.next:
    temp = temp.next

temp.next = node
```

---

## ⏱️ Time Complexity

👉 O(n) (need to traverse list)

---

## ✅ Advantages

✔ Maintains insertion order

---

## ❌ Disadvantages

❌ Slower insertion
❌ Needs traversal

---

# 🔥 Head vs Tail Hashing

| Feature         | Head Hashing | Tail Hashing |
| --------------- | ------------ | ------------ |
| Insert Position | Beginning    | End          |
| Time Complexity | O(1)         | O(n)         |
| Order           | Reversed     | Maintained   |
| Performance     | Faster       | Slower       |

---

