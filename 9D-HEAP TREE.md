# Experiment No: 9D - Python Program to Build and Analyze a Heap Tree

## AIM  
To write a Python program that builds a binary tree from a list and checks whether the tree is a max-heap and a complete tree, and also prints the height of the tree.

## ALGORITHM  
1. Import the necessary modules (`heap`, `Node`, `build`) from the `binarytree` library.
2. Define a function `heaptree(L)` to:
    - Build a binary tree from the list `L`.
    - Print the tree elements.
    - Print the height of the tree.
    - Check and print whether the tree is a max-heap.
    - Check and print whether the tree is a complete tree.
3. Call the function with the given input list to evaluate the tree's properties.

## PROGRAM
```python
from binarytree import heap, Node, build

def heaptree(l):
    t = build(l)
    for i in t.values:
        print(i, "-->", end="")
    print("\nHeight : ", t.height)
    print("Is max heap? : ", t.is_max_heap)
    print("Is complete tree? : ", t.is_complete)

heaptree([89, 81, 76, 22, 14, 9, 54, 11])

```

## OUTPUT
![image](https://github.com/user-attachments/assets/d4e660c9-b0b1-4376-92b5-a0201358d88d)

## RESULT
Thus, the Python program to build a heap tree, check if it is a max-heap and a complete tree, and print its height has been implemented and executed successfully.
