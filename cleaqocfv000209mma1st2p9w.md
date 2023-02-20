# Data Structure Non Linear data structure Tree

**What is a tree?**

A tree is a hierarchical data structure consisting of nodes connected by edges. Each node in the tree can have zero or more child nodes, and each child node can have its own child nodes. The topmost node in the tree is called the root node, and it has no parent node.

Here's an example of what a simple tree might look like:

```plaintext
         A
       /   \
      B     C
     / \   / \
    D   E F   G
```

In this tree, node A is the root node, and it has two child nodes B and C. Node B has two child nodes D and E, and node C has two child nodes F and G. Node D and E are leaf nodes, which means they have no child nodes of their own.

**Terminology of trees**

Here are some important terms related to trees:

* **Node**: A single element in a tree that contains data and references to its child nodes.
    
* **Edge**: The connection between two nodes in a tree.
    
* **Root**: The topmost node in a tree that has no parent nodes.
    
* **Parent**: A node that has one or more child nodes.
    
* **Child**: A node that is directly connected to another node (its parent).
    
* **Siblings**: Nodes that have the same parent.
    
* **Leaf**: A node that has no child nodes.
    
* **Height**: The number of edges on the longest path from a node to a leaf node.
    
* **Depth**: The number of edges from the root node to a node.
    

**Types of trees**

There are many different types of trees, but here are a few common ones:

* **Binary tree**: A tree where each node has at most two child nodes (left and right).
    
* **Binary search tree**: A binary tree where the left child node is less than the parent node, and the right child node is greater than or equal to the parent node.
    
* **AVL tree**: A binary search tree that is balanced, meaning that the heights of the left and right subtrees differ by at most 1.
    
* **Red-black tree**: A binary search tree that is also balanced and has a specific set of rules for maintaining the balance.
    
* **B-tree**: A tree where each node can have multiple child nodes, typically used for file systems and databases.
    

**Tree operations**

Here are some common operations that can be performed on trees:

* **Traversal**: Visiting every node in the tree in a specific order. There are three common ways to traverse a tree: pre-order (visit the node, then the left subtree, then the right subtree), in-order (visit the left subtree, then the node, then the right subtree), and post-order (visit the left subtree, then the right subtree, then the node).
    
* **Search**: Finding a specific node in the tree that matches a given criteria (e.g. finding the node with a specific value).
    
* **Insertion**: Adding a new node to the tree.
    
* **Deletion**: Removing a node from the tree.
    
* **Rotation**: Moving nodes around in the tree to maintain balance (in the case of balanced trees like AVL and red-black trees).
    

I hope this gives you a good overview of trees and their important concepts!

A tree is a nonlinear data structure that consists of nodes connected by edges, forming a hierarchy. Each node in the tree contains a value and has zero or more child nodes. The node at the top of the hierarchy is called the root node, and it has no parent nodes. All other nodes in the tree have exactly one parent node.

Trees are often used in computer science for representing hierarchical relationships. For example, file systems are commonly represented as trees, with the root directory at the top and subdirectories and files as child nodes.

### **Binary Trees**

A binary tree is a type of tree where each node has at most two child nodes, commonly referred to as the left child and the right child. The left child is always less than the parent, and the right child is always greater than or equal to the parent. This property is known as the binary search tree property, and it allows for efficient searching, insertion, and deletion of values.

Here is an example of a binary search tree:

```plaintext
    8
   / \
  3   10
 / \    \
1   6    14
   / \   /
  4   7 13
```

In this tree, the root node has a value of 8, and its left child has a value of 3 and its right child has a value of 10. The left child of 3 has a value of 1 and a right child of 6, and so on.

### **Binary Tree Traversal**

There are three common ways to traverse a binary tree: pre-order, in-order, and post-order.

1. Pre-order traversal visits the node, then its left subtree, and then its right subtree.
    
2. In-order traversal visits the left subtree, then the node, and then the right subtree. In a binary search tree, this will produce a sorted list of the tree's values.
    
3. Post-order traversal visits the left subtree, then the right subtree, and then the node.
    

Here is an example of each type of traversal on the binary search tree above:

```plaintext
Pre-order: 8 3 1 6 4 7 10 14 13
In-order: 1 3 4 6 7 8 10 13 14
Post-order: 1 4 7 6 3 13 14 10 8
```

**Binary Tree Implementation in JavaScript**

Here's an example implementation of a binary search tree in JavaScript:

```javascript
class Node {
  constructor(value) {
    this.value = value;
    this.left = null;
    this.right = null;
  }
}

class BinarySearchTree {
  constructor() {
    this.root = null;
  }

  insert(value) {
    const newNode = new Node(value);
    if (this.root === null) {
      this.root = newNode;
      return this;
    }
    let current = this.root;
    while (true) {
      if (value === current.value) {
        return undefined;
      }
      if (value < current.value) {
        if (current.left === null) {
          current.left = newNode;
          return this;
        }
        current = current.left;
      } else {
        if (current.right === null) {
          current.right = newNode;
          return this;
        }
        current = current.right;
      }
    }
  }

  find(value) {
    if (this.root === null) {
      return undefined;
    }
    let current = this.root;
    while (true) {
      if (value === current.value) {
        return current;
```