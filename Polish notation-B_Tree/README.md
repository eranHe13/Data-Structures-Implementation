# Overview
This repository provides a comprehensive implementation of **Binary Trees** in Java, including full binary trees and expression trees. It includes various operations for tree traversal, evaluation, and conversion. The repository includes:

- **`BinaryTreeI.java`** - Interface defining binary tree operations.
- **`BinaryTree.java`** - Implements a basic binary tree structure.
- **`FullBinaryTree.java`** - Extends `BinaryTree` to represent a full binary tree.
- **`ExpressionTree.java`** - Represents a binary tree for mathematical expressions.
- **`PrePolishToInfix.java`** - Converts prefix expressions to infix.
- **`TestBinaryTree.java`** - Unit tests for `BinaryTree`.
- **`TestFullBinaryTree.java`** - Unit tests for `FullBinaryTree`.

# Features

## Binary Tree Interface (`BinaryTreeI.java`):
- **Key Methods**:
  - `getLeft()`, `getRight()`: Access left or right subtree.
  - `setLeft(BinaryTreeI<T> left)`, `setRight(BinaryTreeI<T> right)`: Set left or right subtree.
  - `getValue()`, `setValue(T value)`: Get or set the value of the root node.
  - `isLeaf()`: Checks if the node is a leaf.
  - `size()`: Returns the number of nodes in the tree.
  - `height()`: Returns the height of the tree.
  - `clear()`: Clears the tree except its root.
  - **Traversal methods**: `preOrder`, `inOrder`, `postOrder` with customizable delimiters.

## Binary Tree (`BinaryTree.java`):
- Implements the `BinaryTreeI` interface.
- Supports operations like traversal, height calculation, and tree size evaluation.
- Customizable pre-order, in-order, and post-order traversals.

## Full Binary Tree (`FullBinaryTree.java`):
- Extends `BinaryTree` to ensure a full binary tree structure.
- Enforces rules for left and right child relationships to maintain tree balance.

## Expression Tree (`ExpressionTree.java`):
- Extends `FullBinaryTree` to evaluate and traverse mathematical expressions.
- **Key Methods**:
  - `createTree(StreamTokenizer tokenizer)`: Builds the tree from a prefix expression.
  - `infix()`: Converts the tree to an infix expression.
  - `prefix()`: Converts the tree to a prefix expression.
  - `evaluate()`: Evaluates the mathematical expression represented by the tree.

## PrePolishToInfix (`PrePolishToInfix.java`):
- Reads a prefix mathematical expression from input.
- Outputs the corresponding infix expression and its evaluated result.
