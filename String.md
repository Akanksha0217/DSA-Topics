# ✅ What is a String?
👉 A string is a sequence of characters
```
s = "hello"
```

##  Properties
- Indexed (starts from 0)
- Ordered
- Immutable (cannot change directly in Python)

## Time Complexity

| Operation        | Complexity |
| ---------------- | ---------- |
| Access character | O(1)       |
| Traverse string  | O(n)       |
| Concatenation    | O(n)       |
| Slicing          | O(n)       |

## Basic Operations
✅ Access
```s[0]```

✅ Traversal
```for ch in s:
    print(ch)
```

✅ Length
```len(s)```

✅ Slicing
```s[1:4]```

✅ Reverse
```s[::-1]```

## Important Functions
- s.lower()
- s.upper()
- s.strip()
- s.replace("a", "b")
- s.split()
- " ".join(list)

## Important Patterns
📝 1. 🔸 Two Pointer Technique

Use two indices (pointers) to traverse data instead of nested loops

🎯 When to Use
- Sorted array/string
- Pair problems (sum, difference)
- Palindrome check
- Reverse operations

📝 2. 🔸 HashMap (Dictionary)
✅ Idea
- Store data as key → value for fast lookup

🎯 When to Use
- Frequency count
- Duplicate detection
- Fast searching (O(1))
- Two Sum problem
