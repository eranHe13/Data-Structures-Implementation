# Overview
This repository provides an implementation of a **Doubly Linked List (DLinkedList)** in Java, along with its interface and comprehensive test files. The repository includes:

- **`List.java`** - Defines the `List` interface for generic list operations.
- **`DLinkedList.java`** - Implements the doubly linked list data structure.
- **`DListFactory.java`** - A factory class to create list instances dynamically.
- **`ListTest.java`** - An abstract test class for generic list testing.
- **`ListTestInteger.java`** - Test class for `DLinkedList` using `Integer` values.
- **`ListTestObject.java`** - Test class for `DLinkedList` using generic `Object` values.

# Features

## List Interface (`List.java`):
- **Generic interface with key list operations**:
  - `insert(T newElement)`: Inserts a new element.
  - `remove()`: Removes the element at the cursor.
  - `remove(T element)`: Removes the first occurrence of a specific element.
  - `clear()`: Clears the entire list.
  - `replace(T newElement)`: Replaces the element at the cursor.
- **Navigation methods**:
  - `goToBeginning()`, `goToEnd()`, `getNext()`, `getPrev()`.
- **Query methods**:
  - `isEmpty()`, `hasNext()`, `hasPrev()`.
- **Accessor**:
  - `getCursor()` returns the current element.

## Doubly Linked List (`DLinkedList.java`):
- **Implements the `List` interface**.
- Maintains bidirectional pointers for efficient traversal in both directions.
- **Key Features**:
  - Supports navigation from the current cursor.
  - Efficiently handles insertion, deletion, and replacement of elements.
  - Custom node class (`DNode`) to encapsulate element, next, and previous references.

## Factory Class (`DListFactory.java`):
- Dynamically generates instances of `List` implementations.
- Default implementation is `DLinkedList`.

## Abstract Test Class (`ListTest.java`):
- Provides a framework for testing list operations.
- Requires subclasses to define the method `getParameterInstance()` to supply test instances.

## Test Classes (`ListTestInteger.java` and `ListTestObject.java`):
- **`ListTestInteger`**:
  - Tests the list using `Integer` values.
  - Generates sequential integers for testing.
- **`ListTestObject`**:
  - Tests the list using generic objects.
  - Ensures object equality and distinctness.
