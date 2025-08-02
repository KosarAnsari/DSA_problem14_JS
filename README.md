# 🚀 Day 14 - Optimized Bubble Sort | 21-Day DSA Challenge

## 📌 Challenge
Refactor the previous Bubble Sort code to make it more efficient by breaking early if the array becomes sorted before all iterations.

---

## 🧠 What I Learned
- Introduced a **`isSwapped` flag** to track if any elements were swapped in a particular pass.
- Used this flag to **exit early** from the loop, optimizing best-case scenarios.
- Understood how **loop optimization** can improve real-world performance of basic sorting algorithms.

---

## 💻 Optimized Code
```javascript
function bubbleSort(array) {
  for (let i = 0; i < array.length; i++) {
    let isSwapped = false;
    for (let j = 0; j < array.length - 1 - i; j++) {
      if (array[j] > array[j + 1]) {
        [array[j], array[j + 1]] = [array[j + 1], array[j]];
        isSwapped = true;
      }
    }
    if (!isSwapped) break;
  }
  return array;
}


---

🧪 Example

Input:

[8, 1, 2, 3, 4, 5, 6, 7]

Output:

[1, 2, 3, 4, 5, 6, 7, 8]


---

🧩 Key Benefits of Optimization

Reduces unnecessary passes in already sorted or nearly sorted arrays

Improves performance for best-case time complexity from O(n²) to O(n)

Builds habit of writing efficient, readable, and maintainable code



---

🔖 Tags

#JavaScript #DSA #BubbleSort #Optimization #SortingAlgorithm #21DaysOfDSA

