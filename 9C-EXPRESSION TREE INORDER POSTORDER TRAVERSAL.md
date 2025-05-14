# Experiment No: 9C - Python Program to Build and Evaluate an Expression Tree

## AIM  
To write a Python program that builds and evaluates an expression tree using recursion.

## ALGORITHM  
1. Define a `Node` class to represent the nodes of the expression tree, with attributes for value (`val`), left child (`left`), and right child (`right`).
2. Define the `isLeaf()` function to check if a node is a leaf (i.e., it has no children).
3. Define the `process()` function to perform arithmetic operations (`+`, `-`, `*`, `/`) based on the operator passed.
4. Define the `evaluate()` function that recursively evaluates the expression tree. If the node is a leaf, return its value as a float; otherwise, recursively evaluate its left and right children, and apply the operator at the current node.
5. Build the expression tree based on the given structure.
6. Print the value of the expression tree after evaluation.

## PROGRAM
```python
class Node:
    def __init__(self, val, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

def isLeaf(node):
    return node.left is None and node.right is None

def process(op, x, y):
    if op == '+':
        return x + y
    if op == '-':
        return x - y
    if op == '*':
        return x * y
    if op == '/':
        return x / y

def evaluate(root):
    if root is None:
        return 0

    if isLeaf(root):
        return float(root.val)
    
    x = evaluate(root.left)
    y = evaluate(root.right)
    return process(root.val, x, y)

root = Node('+')
root.left = Node(3)
root.right = Node('*')
root.right.left = Node('+')
root.right.right = Node(2)
root.right.left.left = Node(5)
root.right.left.right = Node(9)

print('The value of the expression tree is', evaluate(root))

```

## OUTPUT
![image](https://github.com/user-attachments/assets/9d09e700-a059-4dd3-aa7e-a01cdb96ddf5)

## RESULT
Thus, the Python program to build and evaluate an expression tree using recursion has been implemented and executed successfully.
