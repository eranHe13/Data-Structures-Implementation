# Overview
This project provides an implementation of a **Diagonal Matrix** in Java, along with its interface and associated test files. The repository includes:

- **`Matrix.java`** - Defines an interface for matrix operations.
- **`DiagonalMatrix.java`** - Implements a specialized diagonal matrix.
- **`DiagonalMatrixTest.java`** - Provides unit tests for the diagonal matrix implementation.

# Features

## Matrix Interface (`Matrix.java`):
- **Defines the following operations**:
  - `get(int i, int j)`: Retrieves the value at position `(i, j)`.
  - `set(int i, int j, double x)`: Updates the value at position `(i, j)` to `x`.
  - `transpose()`: Replaces the current matrix with its transpose.
  - `getTranspose()`: Returns a new matrix that is the transpose of the current matrix.
- **Includes a constant** `MAX_SIZE` set to 100.

## Diagonal Matrix (`DiagonalMatrix.java`):
- **Implements the `Matrix` interface** specifically for diagonal matrices.
- **Key Features**:
  - Optimized storage using a 1D array for efficiency.
  - Handles transpose operations and returns either an updated or a new transposed matrix.
  - Ensures efficient access and modification of elements.
- **Constructors**:
  - `DiagonalMatrix(int size)`: Initializes a matrix of size `size * size`.
  - `DiagonalMatrix()`: Initializes a matrix of size `MAX_SIZE * MAX_SIZE`.
- **Methods**:
  - `toString()`: Converts the matrix into a string representation with tab-separated rows.

## Testing (`DiagonalMatrixTest.java`):
- **Comprehensive unit tests** for diagonal matrix functionality.
- **Key Tests**:
  - `testDiagonalMatrixInt`: Validates diagonal matrix creation and access outside bounds.
  - `testGetSet`: Ensures correctness of setting and getting values.
  - `testTranspose`: Validates in-place transpose functionality.
  - `testGetTranspose`: Verifies the creation of a new transposed matrix.
  - `testToString`: Checks the string representation of the matrix.
