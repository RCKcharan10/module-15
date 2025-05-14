# Experiment No: 9A - Python Program to Print a Binary Tree Consisting of Root, Left, and Right Nodes

## AIM  
To write a Python program that prints a binary tree consisting of a root, left, and right node.

## ALGORITHM  
1. Import the `Node` class from the `binarytree` library.
2. Create a list to store node values.
3. Take input from the user to fill the node values and append them to the list.
4. Create a root node with the first element of the list.
5. Assign the left and right children of the root using the second and third elements of the list respectively.
6. Print the binary tree structure by iterating through the node values.

## PROGRAM
```python
from binarytree import Node

l = []

for i in range(3):
    l.append(input())
    
root = Node(l[0])
root.left = Node(l[1])
root.right = Node(l[2])

print("Binary Tree : ")
for i in root.values:
    print(i, "--> ", end="")
```

## OUTPUT
![image](https://github.com/user-attachments/assets/b20d1929-3c96-43f4-9a5d-5390ebfe0849)

## RESULT
Thus, the Python program to print a binary tree consisting of a root, left, and right node has been implemented and executed successfully.
