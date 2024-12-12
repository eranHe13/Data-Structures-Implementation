# Overview
This repository provides an implementation of a **MinHeap** in Java. The heap supports generic types and offers efficient insertion, retrieval, and deletion of the minimum element. The repository includes:

- **`MinHeap.java`** - Implements the min-heap data structure.
- **`Person.java`** - Represents a person with attributes (`id`, `firstName`, `lastName`).
- **`MinHeapTest.java`** - Unit tests for the min-heap implementation.

# Features

## MinHeap (`MinHeap.java`):
- **Key Features**:
  - Supports generic types that implement `Comparable`.
  - Efficiently maintains heap properties during insertion and deletion.
- **Constructors**:
  - `MinHeap(int length)`: Initializes an empty heap with a specified maximum size.
  - `MinHeap(T[] arr)`: Builds a heap from an existing array, ensuring the heap property.
- **Methods**:
  - `insert(T element)`: Inserts an element into the heap, maintaining the heap property.
  - `getMin()`: Retrieves the minimum element without removing it.
  - `deleteMin()`: Removes and returns the minimum element.
  - `isFull()`: Checks if the heap is full.
  - `isEmpty()`: Checks if the heap is empty.
  - `toString()`: Returns a string representation of the heap.

## Person Class (`Person.java`):
- **Represents a person** with attributes `id`, `firstName`, and `lastName`.
- **Implements `Comparable`** to allow comparison by `id`.
- **Overrides**:
  - `toString()`: Provides a readable string representation.
  - `compareTo()`: Compares `Person` objects based on their `id`.

## MinHeap Tests (`MinHeapTest.java`):
- **Comprehensive unit tests** for the min-heap implementation.
- **Key Tests**:
  - Verifies insertion of elements while maintaining the heap property.
  - Tests retrieval of the minimum element with `getMin`.
  - Validates removal of elements with `deleteMin`.
  - Checks for edge cases such as empty or full heaps.
  - Ensures heap construction from an array maintains heap order.
