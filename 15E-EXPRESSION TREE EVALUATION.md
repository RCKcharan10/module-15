# Experiment No: 15E - Python Program to Build and Evaluate an Expression Tree

## AIM  
To write a Python program to construct an expression tree and evaluate its result using recursion.

## ALGORITHM  
1. Define a `Node` class with attributes `val`, `left`, and `right`.
2. Define the function `isLeaf(node)` to check whether the node is a leaf node.
3. Define the function `process(op, x, y)` to perform arithmetic operations.
4. Define the function `evaluate(root)`:
   - If the node is a leaf, return its float value.
   - Recursively evaluate the left and right subtrees.
   - Perform the operation on evaluated left and right values.
5. Build the expression tree manually by creating nodes and linking them.
6. Call the `evaluate()` function with the root node to evaluate the expression tree.

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
    return (process(root.val, x, y))

root = Node('+')
root.left = Node('*')
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(8)

print('The value of the expression tree is', evaluate(root))

```

## OUTPUT
![image](https://github.com/user-attachments/assets/35cdb0cd-edca-4b9f-8473-789c6265c535)


## RESULT
Thus, the expression tree is constructed and evaluated successfully using recursion.
