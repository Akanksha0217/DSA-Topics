# 🔹 Hashing – Complete Notes (DSA)

## 🔹 What is Hashing?

Hashing is a technique used to store and retrieve data **quickly using keys**

👉 It maps:

```
key → value
```

---

## 🔹 Data Structures Used

* HashMap (Dictionary in Python)
* HashSet (Set in Python)

---

## 🔹 Why Hashing?

👉 Fast operations:

* Insert → O(1)
* Search → O(1)
* Delete → O(1)

---

## 🔹 Example

```python
data = {
    "a": 1,
    "b": 2
}
```

👉 Access:

```python
print(data["a"])  # 1
```

---

## 🔹 HashMap vs HashSet

| Feature    | HashMap     | HashSet       |
| ---------- | ----------- | ------------- |
| Stores     | Key → Value | Only values   |
| Duplicates | Keys unique | No duplicates |
| Example    | dict        | set           |

---

## 🔹 Basic Operations

### ✅ Insert

```python
d = {}
d["a"] = 1
```

### ✅ Search

```python
if "a" in d:
    print("Found")
```

### ✅ Delete

```python
del d["a"]
```

---

## 🔹 Common Problems

---

### 🔸 1. Frequency Count

```python
s = "hello"

freq = {}
for ch in s:
    freq[ch] = freq.get(ch, 0) + 1

print(freq)
```

---

### 🔸 2. Check Duplicates

```python
arr = [1, 2, 3, 2]

seen = set()

for num in arr:
    if num in seen:
        print("Duplicate found")
    seen.add(num)
```

---

### 🔸 3. Two Sum Problem 🔥

```python
arr = [2, 7, 11, 15]
target = 9

map = {}

for i in range(len(arr)):
    diff = target - arr[i]
    
    if diff in map:
        print("Found pair")
    
    map[arr[i]] = i
```

---

## 🔹 Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| Insert    | O(1)       |
| Search    | O(1)       |
| Delete    | O(1)       |

👉 Worst case can be O(n), but rare

---

## 🔹 Internal Working (Basic Idea)

👉 Hash Function:

```
key → index
```

Example:

```
"h" → 104 → index
```

---

## 🔹 Collision (Important)

👉 When two keys map to same index

### Handling:

* Chaining
* Open Addressing

---

## 🔹 When to Use Hashing

✔ Frequency counting
✔ Fast lookup
✔ Removing duplicates
✔ Pair problems

---

## 🔹 When NOT to Use

❌ When order matters
❌ When sorting is required

---

## 🔹 Common Mistakes

❌ Not checking key exists
❌ Overwriting values
❌ Forgetting edge cases

---


* "count frequency" → use hashmap
* "find duplicate" → use set
* "pair sum" → hashmap

---


---

