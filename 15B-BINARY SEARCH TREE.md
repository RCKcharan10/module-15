# Experiment No: 15B - Python Program to Build a Binary Search Tree Using a Built-in Function

## AIM  
To write a Python program to build a binary search tree (BST) using a built-in function and perform postorder traversal, print the left subtree, and verify whether the tree is a Binary Search Tree.

## ALGORITHM  
1. Import the necessary classes (`Node`, `build`) from the `binarytree` module.
2. Define a recursive function `_build_bst_from_sorted_values()` that builds a binary search tree from a sorted list.
3. Define the `left_subtree()` function to print the left subtree of the BST.
4. Get the size and values for the BST nodes from the user and sort the list.
5. Build the BST using the sorted values.
6. Print the postorder traversal of the BST.
7. Print the left subtree of the BST.
8. Check and print whether the tree is a Binary Search Tree.

## PROGRAM
```python
from binarytree import Node

def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values) == 0:
        return None
    mid_index = len(sorted_values) // 2
    root = Node(sorted_values[mid_index])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right = _build_bst_from_sorted_values(sorted_values[mid_index + 1 :])  
    return root

def left_subtree(l):
    for i in l.left.values:
        print(i, "-->", end="")
    return 

a = []
size = int(input())
for i in range(0, size):
    val = int(input())
    a.append(val)
x = sorted(a)

l = _build_bst_from_sorted_values(x)
print("Postorder :", l.postorder)
print("Left Subtree :")
left_subtree(l)
print("\nIs this a Binary Search Tree? ", l.is_bst)

```

## OUTPUT
![image](https://github.com/user-attachments/assets/7cf1a49e-48c9-4a08-82fe-4fdb87f2c737)


## RESULT
Thus, the Python program to build a binary search tree using a built-in function and perform postorder traversal has been implemented and executed successfully. The left subtree was printed, and it was verified that the tree is a Binary Search Tree.
