# Ex. No: 15C - Expression Tree with Inorder and Postorder Traversal

## AIM:
To write a Python program to build the given expression tree and print the inorder and postorder traversals.

---

## ALGORITHM:

1. **Start the program.**
2. Import the required modules (`build` and `Node` from `binarytree`).
3. Define a list `x` representing the expression tree in pre-order fashion (with `None` for missing nodes).
4. Use the `build()` function to generate the binary tree.
5. Print the **inorder** and **postorder** traversal of the tree.
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
return (process(root.val, x, y))
root = Node('+')

root.left = Node('*')

root.right = Node(3)

root.left.left = Node(4)

root.left.right = Node(8)

print('The value of the expression tree is', evaluate(root))
```

## OUTPUT
![image](https://github.com/user-attachments/assets/972370ba-7d62-4cbb-917b-07127edc9b42)


## RESULT
Thus, the expression tree is constructed and evaluated successfully using recursion.
