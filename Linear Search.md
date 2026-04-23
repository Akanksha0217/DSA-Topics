# 📝 1. Linear Search (Detailed Explanation)
✅ Basic Idea

👉 Check each element one by one from start to end until you find the target.

# 🔹 How It Works (Step-by-Step)

- Example:

```
arr = [10, 20, 30, 40]
target = 30
```

## 🔍 Steps:
- Compare 10 with 30 ❌
- Compare 20 with 30 ❌
- Compare 30 with 30 ✅ → Found!

👉 Stop immediately when found

## ⏱️ Time Complexity 

1) Worst Case:
👉 When element is at last or not present

2) Best Case:
👉 When element is at first position


## 📊 Example Cases

| Case    | Input        | Steps   |
| ------- | ------------ | ------- |
| Best    | [30, 10, 20] | 1 step  |
| Average | [10, 30, 20] | ~n/2    |
| Worst   | [10, 20, 40] | n steps |

##  🎯 When Should You Use Linear Search?

- ✔ Array is unsorted
- ✔ Small input size
- ✔ No need for optimization

## ❌ When NOT to Use

- 🚫 Large data (slow)
- 🚫 When faster method (Binary Search) is possible
