# What is Space Complexity?

It tells you how much memory your algorithm uses

# Types of Space

 ## 1. Input Space
Memory used to store input

 ## 2. Auxiliary Space
Extra memory used (important in interviews)


### 🔥 Time vs Space Trade-off
- Faster code may use more memory
- Less memory may take more time

👉 You need to balance both

### Example: Calculator (Space Complexity)
✅ Case 1: Simple Calculator (No Extra Memory)
def add(a, b):
    return a + b
🔍 Space Complexity:

- Uses only 2 variables (a, b)
- No extra data structures

👉 Space = O(1) (Constant space)

✅ Case 2: Calculator with Storing History
def calculator_history(arr):
    result = []
    for i in arr:
        result.append(i * 2)
    return result
🔍 Space Complexity:
- Input size = n
- New list result also grows with n

👉 Space = O(n)

✔ Because we are storing results

# 🧠 Rule:
- No extra memory → O(1)
- Using array/list/dictionary → O(n)
