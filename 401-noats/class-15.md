# class 15

## Common Terminology

- *Node* - A Tree node is a component which may contain its own values, and references to other nodes
- *Root* - The root is the node at the beginning of the tree
- *K* - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, **`k = 2`**.
- *Left* - A reference to one child node, in a binary tree
- *Right* - A reference to the other child node, in a binary tree
- *Edge* - The edge in a tree is the link between a parent and child node
- *Leaf* - A leaf is a node that does not have any children
- *Height* - The height of a tree is the number of edges from the root to the furthest leaf

There are two types of traversal: Depth First and Breadth First.

Depth first traversal is prioritizes going through the depth (height) of the tree first.

Here are three methods for depth first traversal:

- Pre-order: **`root >> left >> right`**
- In-order: **`left >> root >> right`**
- Post-order: **`left >> right >> root`**

### Breadth First

Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

Trees can have any number of children per node, but Binary Trees restrict the number of children to two.

If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use **`K`** to refer to the maximum number of children that each Node is able to have.

A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the **`root`** are placed to the left, and all values that are larger than the **`root`** are placed to the right.

Here is how we would change our Binary Tree example into a Binary Search Tree:

The Big O time complexity of a Binary Search Tree’s insertion and search operations is **`O(h)`**, or **`O(height)`**. In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is **`log(n)`**. In an unbalanced tree, the worst case height of the tree is **`n`**.

The Big O space complexity of a BST search would be **`O(1)`**. During a search, we are not allocating any additional space.
