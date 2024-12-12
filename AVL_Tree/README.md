# Overview
This project implements an AVL Tree, a self-balancing binary search tree, in Java. The repository contains two main files:

- **`AVLTree.java`** - Implements the core functionality of the AVL Tree.
- **`TestAVLTree.java`** - Provides unit tests to verify the correctness of the AVL Tree implementation.

# Features
- **Automatic Tree Balancing**: Ensures that the tree remains balanced after every insertion.
- **Rotations**: Includes single and double rotations (LL, RR, LR, RL) to maintain balance.
- **Tree Properties**:
  - **Height Calculation**: Efficiently computes the height of each node.
  - **Size Maintenance**: Tracks the size (number of nodes) under each subtree.
- **Utility Methods**:
  - Get the value of a node.
  - Access left and right child nodes.

# File Descriptions

## `AVLTree.java`

- **Core Class**: Implements the AVL Tree as a generic class supporting any comparable type (`T extends Comparable<T>`).
- **Key Methods**:
  - `add(T value)`: Inserts a value into the AVL Tree while maintaining its balance.
  - `updateHeight()`: Updates the height of the node based on its children.
  - `updateSize()`: Updates the size of the subtree rooted at the node.
  - `checkBalance()`: Checks the balance factor of a node.
  - Rotation methods (`LEFT_LEFT`, `RIGHT_RIGHT`, `LEFT_RIGHT`, `RIGHT_LEFT`): Handle tree rebalancing scenarios.
- **Properties**:
  - `val`: Value stored in the node.
  - `height`: Height of the subtree rooted at the node.
  - `size`: Size of the subtree rooted at the node.
  - `left` and `right`: References to child nodes.

## `TestAVLTree.java`

- **Unit Tests**:
  - Verifies tree structure after insertion of nodes.
  - Tests single and double rotations to ensure the tree remains balanced.
- **Helper Methods**:
  - `inOrder(AVLTree<T> tree)`: Produces an in-order traversal string of the tree.
  - `checkTreeStructure(AVLTree<Integer> tree)`: Validates the tree structure.

# Author
**Eran Helvitz** - Original implementation of the AVL Tree.
