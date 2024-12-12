# Overview
This repository provides an implementation of a **Binary Search Tree (BST)** and a **Person** class in Java. It also includes test files to verify the correctness of these implementations. The repository is organized into the following key files:

- **`BinarySearchTree.java`** - Implements a generic Binary Search Tree.
- **`Person.java`** - Represents a person with attributes and comparison logic.
- **`PersonTest.java`** - Tests the functionality of the `Person` class.
- **`TestBinarySearchTreeInteger.java`** - Verifies the BST using `Integer` values.
- **`TestBinarySearchTreePerson.java`** - Verifies the BST using `Person` objects.

# Features

## Binary Search Tree:
- **Generic implementation** supporting any comparable type (`T extends Comparable<T>`).
- **Insert, remove, and search** operations with balanced binary search properties.
- Methods for **finding the smallest element** greater than or equal to a given value.
- Tracks the **number of nodes** in the tree.

## Person Class:
- **Customizable attributes**: `id`, `firstName`, and `lastName`.
- Implements **`Comparable`** for ordering by `id`.
- Overrides **`equals`**, **`hashCode`**, and **`toString`** for better usability.

# File Descriptions

## `BinarySearchTree.java`:
- **Implements the core functionality** of a BST.
- **Key Methods**:
  - `add(T val)`: Adds a new element while maintaining BST properties.
  - `remove(T val)`: Removes an element if it exists in the tree.
  - `contains(T val)`: Checks if an element exists in the tree.
  - `findGe(T val)`: Finds the smallest element greater than or equal to `val`.
- **Utility Methods**:
  - `isLeaf()`: Checks if a node is a leaf.
  - `getValInPath(Direction... direction)`: For testing purposes, retrieves a value following a specified path.

## `Person.java`:
- **Represents a `Person`** with attributes for `id`, `firstName`, and `lastName`.
- Implements **`Comparable`** to compare `Person` objects by their `id`.
- **Overrides methods**:
  - `equals`: Ensures equality is based on `id`.
  - `hashCode`: Generates a hash code based on `id`.
  - `toString`: Provides a formatted string representation.

## `PersonTest.java`:
- **Tests the `Person` class** for functionality, including:
  - Attribute manipulation (e.g., `setFirstName`, `setLastName`).
  - Comparison (`compareTo`) and equality (`equals`).
- **Includes edge cases** for attributes and comparison logic.

## `TestBinarySearchTreeInteger.java`:
- **Tests the BST implementation** with `Integer` values.
- **Key Tests**:
  - Adding and removing elements.
  - Verifying the BST structure and size.
  - Testing `findGe` functionality with edge cases.

## `TestBinarySearchTreePerson.java`:
- **Tests the BST implementation** with `Person` objects.
- **Key Tests**:
  - Adding and removing `Person` objects.
  - Validating BST behavior with custom objects.
  - Ensures correctness of `findGe` for `Person` attributes.

# Author
**Eran Helvitz** - Original implementation of the `Person` and `BinarySearchTree`.
