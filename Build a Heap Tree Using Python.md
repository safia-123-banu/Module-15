# Ex. No: 15D - Build a Heap Tree Using Python

## AIM:
To write a Python program to build a heap tree using appropriate Python package and function.

---

## ALGORITHM:

1. **Start the program.**
2. Import the `heapq` module.
3. Define a function `heaptree(H)` that takes a list `H` as input.
4. Use `heapq.heapify(H)` to convert the list into a min-heap.
5. Print the created heap.
6. **End the program.**

---

## PROGRAM:

```
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
![image](https://github.com/user-attachments/assets/5f305ed4-5ba3-4224-b396-cb77f97ebd1b)


## RESULT
Thus, the Python program to build and evaluate an expression tree using recursion has been implemented and executed successfully.
