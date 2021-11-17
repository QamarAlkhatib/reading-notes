# Tree

Common Terminology

- Node - A Tree node is a component which may contain it’s own values, and references to other nodes
- Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
Height - The height of a tree is the number of edges from the root to the furthest leaf


Example:

![tree](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)


---

## Traversals

Traversing a tree allows us to search for a node, print out the contents of a tree, and much more.

Types of traversals:

- Depth-first traversal
- Breadth-first traversal

### Depth-first traversal

Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the ```root```. Here are three methods for depth first traversal:


* Pre-order: ```root >> left >> right```
* In-order: ```left >> root >> right```
* Post-order: ```left >> right >> root```

Here is a simple example:
![example](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)


* Pre-order: ```A, B, D, E, C, F```
* In-order: ```D, B, E, A, F, C```
* Post-order: ```D, E, B, F, C, A```


----  

## Algorithm pseudocode:

- pre-order: 

```python
ALGORITHM preOrder(root)

  OUTPUT <-- root.value

  if root.left is not NULL
      preOrder(root.left)

  if root.right is not NULL
      preOrder(root.right)

```

- In-order

```python

ALGORITHM inOrder(root)
# INPUT <-- root node
# OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)
```

- Post-order

```python
ALGORITHM postOrder(root)
#// INPUT <-- root node
#// OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value

```


- I will do the rest in the weekend