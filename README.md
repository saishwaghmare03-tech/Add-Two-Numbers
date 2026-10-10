# Add-Two-Numbers

This project contains a Java implementation for the classic [LeetCode 2. Add Two Numbers](https://leetcode.com/problems/add-two-numbers/) problem, along with utility methods and a `main` method to easily test the solution locally.

## 📌 Problem Statement

You are given two non-empty linked lists representing two non-negative integers. The digits are stored in **reverse order**, and each of their nodes contains a single digit. Add the two numbers and return the sum as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

### Example 1:
* **Input:** `l1 = [2,4,3]`, `l2 = [5,6,4]`
* **Output:** `[7,0,8]`
* **Explanation:** `342 + 465 = 807` (represented in reverse order as `7 -> 0 -> 8`).

---

## 💡 Approach & Algorithm

1. **Reverse Order Traversal:** Because the digits are stored in reverse order, the least significant digit (ones place) comes first. This allows us to perform elementary school-style addition from left to right, carrying over values as we go.
2. **Dummy Head Pointer:** A dummy head node is used to simplify the creation of the result linked list and avoid edge cases with empty pointers.
3. **Loop Condition:** We traverse both linked lists simultaneously as long as there are nodes remaining in `l1`, `l2`, or there is a leftover `carry` value.
4. **Digit Calculation:** At each step, we sum the values of current nodes plus the `carry`, calculate the new `carry` (`sum / 10`), and append the digit (`sum % 10`) to our result list.

---

## ⚡ Complexity Analysis

* **Time Complexity:** $O(\max(N, M))$ where $N$ and $M$ are the lengths of the two linked lists. We iterate through both lists at most once.
* **Space Complexity:** $O(\max(N, M))$ for allocating space to store the new resulting linked list.

---

## 🚀 How to Run Locally

### Prerequisites
* Java Development Kit (JDK) installed on your system.

### Steps
1. Save the code into a file named **`Solution.java`**.
2. Open your terminal or command prompt in the directory where the file is saved.
3. Compile the Java file:
   ```bash
   javac Solution.java
