# Ex. No: 15E - Build and Evaluate an Expression Tree

## AIM:
To write a Python program to build and evaluate the given Expression tree.

---

## ALGORITHM:

1. **Start the program.**
2. Create nodes for operators and operands.
3. Build the expression tree by connecting nodes in the correct hierarchical structure.
4. Define a recursive function `evaluate(root)`:
   - If the node is a number (leaf), return it.
   - Else, recursively evaluate left and right subtrees.
   - Apply the operator at the current node to the results.
5. Return the final result from the root node.
6. **End the program.**

---

## PROGRAM:

```
from binarytree import heap, Node, build.

def heaptree(l):

t = build(l)

for i in t.values:

    print(i, "-->", end="")
    
print("\nHeight : ", t.height)

print("Is max heap? : ", t.is_max_heap)

print("Is complete tree? : ", t.is_complete)
heaptree([89, 81, 76, 22, 14, 9, 54, 11])
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/5c1e6e16-9126-4e75-8063-9f6a97c95fa5)


## RESULT:
Thus, the Python program to build a heap tree, check if it is a max-heap and a complete tree, and print its height has been implemented and executed successfully.

