# 🔁 Recursion Functions 

## 🔹 What is Recursion?

Recursion is a technique where a **function calls itself** to solve smaller parts of a problem.

---

## 🔹 Basic Structure of Recursive Function

```python
def function_name(parameters):
    # Base Case (stopping condition)
    if condition:
        return value
    
    # Recursive Case
    return function_name(smaller_input)
```

---

## 🔹 Two Important Parts

### 1. Base Case 🔴

👉 Stops recursion
👉 Prevents infinite loop

---

### 2. Recursive Case 🔁

👉 Function calls itself with smaller input

---

## 🔹 Example 1: Factorial

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n-1)
```

### Explanation:

```text
factorial(3)
= 3 * factorial(2)
= 3 * 2 * factorial(1)
= 3 * 2 * 1 * factorial(0)
= 3 * 2 * 1 * 1 = 6
```

---

## 🔹 Example 2: Fibonacci

```python
def fib(n):
    if n <= 1:
        return n
    return fib(n-1) + fib(n-2)
```

---

## 🔹 How Recursion Works 

👉 Each function call goes into a **stack**

```text
fib(3)
→ fib(2)
→ fib(1)
→ fib(0)
```

Then returns back step by step

---

## 🔹 Time Complexity

* Factorial → O(n)
* Fibonacci → O(2ⁿ)

---

## 🔹 Space Complexity

👉 Due to function call stack:

* O(n)

---

## 🔹 Types of Recursion

### 🔸 1. Direct Recursion

Function calls itself

---

### 🔸 2. Indirect Recursion

Function A → Function B → Function A

---

### 🔸 3. Tail Recursion

Recursive call is last statement

```python
def func(n):
    if n == 0:
        return
    return func(n-1)
```

---

## 🔹 Common Problems

* Factorial
* Fibonacci
* Sum of array
* Reverse string
* Print numbers

---

## 🔹 Example: Sum of Array

```python
def sum_array(arr, n):
    if n == 0:
        return 0
    return arr[n-1] + sum_array(arr, n-1)
```

---

## 🔹 When to Use Recursion?

✔ Problem can be broken into smaller subproblems
✔ Tree / Graph problems
✔ Divide & Conquer

---

## 🔹 When NOT to Use

❌ Large input with deep recursion
❌ When iterative solution is simpler

---

## 🔹 Common Mistakes

❌ Missing base case
❌ Infinite recursion → Stack Overflow
❌ Not reducing problem size

---

## 🔹 Recursion vs Iteration

| Feature | Recursion    | Iteration |
| ------- | ------------ | --------- |
| Code    | Short        | Longer    |
| Memory  | More (stack) | Less      |
| Speed   | Slower       | Faster    |

---

## 🔹 Optimization (Important 🔥)

👉 Use **Memoization (DP)**

```python
def fib(n, dp={}):
    if n in dp:
        return dp[n]
    if n <= 1:
        return n
    dp[n] = fib(n-1, dp) + fib(n-2, dp)
    return dp[n]
```
