# 🔗 Linked List
## 🔹 What is a Linked List?

A Linked List is a linear data structure where elements are stored as **nodes**.

Each node contains:

1. Data
2. Address of next node

---

## 🔹 Structure of Node

```text id="1a9cd7"
[data | next]
```

Example:

```text id="4hf7b2"
[10|*] → [20|*] → [30|None]
```

---

## 🔹 Why Linked List?

Arrays have fixed size and shifting cost.

Linked List solves:

* Dynamic size ✅
* Easy insertion/deletion ✅

---

## 🔹 Node Example (Python)

```python id="t6v1qp"
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```

---

## 🔹 Creating Linked List

```python id="c2k8mj"
head = Node(10)
second = Node(20)
third = Node(30)

head.next = second
second.next = third
```

Structure:

```text id="5u0f9e"
10 → 20 → 30
```

---

# 🔹 Types of Linked List

---

## 1. Singly Linked List

Each node points to next node only.

```text id="r7n3tx"
10 → 20 → 30 → None
```

---

## 2. Doubly Linked List

Each node has:

* previous
* next

```text id="q5m1kc"
None ← 10 ⇄ 20 ⇄ 30 → None
```

---

## 3. Circular Linked List

Last node points back to first.

```text id="d4g9vb"
10 → 20 → 30
↑       ↓
└───────┘
```

---

# 🔹 Operations

---

## 1. Traversal

```python id="ax0mws"
temp = head
while temp:
    print(temp.data)
    temp = temp.next
```

---

## 2. Insertion at Beginning

```python id="mx8qrl"
new_node = Node(5)
new_node.next = head
head = new_node
```

---

## 3. Insertion at End

```python id="px3hjt"
temp = head
while temp.next:
    temp = temp.next

temp.next = Node(40)
```

---

## 4. Deletion

Delete first node:

```python id="7jql5a"
head = head.next
```

---

# 🔹 Time Complexity

| Operation           | Complexity |
| ------------------- | ---------- |
| Access              | O(n)       |
| Search              | O(n)       |
| Insert at beginning | O(1)       |
| Delete at beginning | O(1)       |

---

# 🔹 Array vs Linked List

| Feature       | Array      | Linked List    |
| ------------- | ---------- | -------------- |
| Memory        | Continuous | Non-continuous |
| Access        | O(1)       | O(n)           |
| Insert/Delete | Slow       | Fast           |

---

# 🔹 Advantages

✔ Dynamic size
✔ Easy insertion/deletion

---

# 🔹 Disadvantages

❌ Extra memory for pointers
❌ No direct indexing

---



