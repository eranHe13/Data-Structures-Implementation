# Overview
This repository provides an implementation of a **Sparse Matrix** in Java. The sparse matrix is optimized for storage and operations on matrices with a majority of default values. It includes the following components:

- **`Matrix.java`** - Interface defining matrix operations.
- **`SparseMatrix.java`** - Implements the sparse matrix.
- **`MatrixFactory.java`** - Factory class to generate instances of `Matrix`.
- **`DLinkedList.java`** - Doubly linked list implementation used by the sparse matrix.
- **`List.java`** - Interface defining list operations.
- **`MatrixTest.java`** - Unit tests for the matrix implementation.

# Features

## Matrix Interface (`Matrix.java`):
- **Key Methods**:
  - `T get(int row, int col)`: Retrieves the value at the specified position.
  - `void set(int row, int col, T element)`: Updates the value at the specified position.
  - `void transpose()`: Transposes the matrix (should run in \(O(1)\) time).
- **Includes** a constant `MAX_SIZE` set to `100`.

## Sparse Matrix (`SparseMatrix.java`):
- **Key Features**:
  - Uses a doubly linked list to store non-default values.
  - Supports efficient retrieval, insertion, and updating of values.
  - Implements `transpose()` by toggling a boolean flag.
- **Inner Class**:
  - `SparseMatrixEntry`: Represents a non-default matrix entry with `row`, `col`, and `value`.

## Matrix Factory (`MatrixFactory.java`):
- Dynamically generates instances of the `Matrix` interface.
- Supports creation with or without a specified size.

## Doubly Linked List (`DLinkedList.java`):
- **Implements** the `List` interface.
- **Key Features**:
  - Provides efficient insertion, deletion, and traversal operations.
  - Used by the `SparseMatrix` to manage non-default entries.

## List Interface (`List.java`):
- **Key Operations**:
  - `insert(T newElement)`: Inserts a new element into the list.
  - `remove()`: Removes the current element.
  - `clear()`: Clears all elements from the list.
  - `replace(T newElement)`: Replaces the current element with a new one.
  - Navigation and access methods: `getNext()`, `getPrev()`, `getCursor()`.

## Matrix Tests (`MatrixTest.java`):
- **Comprehensive unit tests** for the matrix implementation.
- **Key Tests**:
  - Validates size restrictions and exception handling for out-of-bounds indices.
  - Tests `get` and `set` methods with various values.
  - Verifies `transpose()` functionality.
  - Ensures default values are properly maintained.
