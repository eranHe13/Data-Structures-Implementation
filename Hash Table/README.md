# Overview
This repository provides an implementation of a **Hash Table** in Java. The implementation supports generic types and uses a **Doubly Linked List (DLinkedList)** for handling collisions via chaining. The repository includes:

- **`HashTable.java`** - Implements a generic hash table.
- **`DLinkedList.java`** - Implements a doubly linked list.
- **`List.java`** - Interface defining the operations for a list.
- **`Person.java`** - Represents a person with attributes (`id`, `firstName`, and `lastName`).
- **`HashTableTest.java`** - Unit tests for the hash table.

# Features

## Hash Table (`HashTable.java`):
- **Key Features**:
  - Generic implementation supporting any type with a properly implemented `hashCode` and `equals` method.
  - Uses chaining for collision resolution with the help of a doubly linked list.
- **Constructors**:
  - Default constructor initializes the hash table with a size of `10`.
  - Custom constructor allows specifying the size of the hash table.
- **Methods**:
  - `add(V val)`: Adds a value to the hash table.
  - `remove(V val)`: Removes a value from the hash table.
  - `contains(V val)`: Checks if a value exists in the hash table.
  - `clear()`: Clears all entries in the hash table.
  - `isEmpty()`: Checks if the hash table is empty.

## Doubly Linked List (`DLinkedList.java`):
- **Implements the `List` interface**.
- **Key Features**:
  - Efficient traversal with `next` and `previous` pointers.
  - Supports insertion, deletion, and replacement of elements.
- **Methods**:
  - `insert(T newElement)`: Inserts a new element.
  - `remove()`: Removes the element at the cursor.
  - `remove(T element)`: Removes the first occurrence of a specific element.
  - `clear()`: Clears the list.
  - `goToBeginning()`, `goToEnd()`: Moves the cursor to the start or end of the list.
  - `getNext()`, `getPrev()`: Retrieves the next or previous element.

## List Interface (`List.java`):
- **Defines operations for generic list implementations**, including:
  - `insert`, `remove`, `clear`, `replace`.
  - Navigation (`goToBeginning`, `goToEnd`, `getNext`, `getPrev`).
  - Access (`getCursor`), and query methods (`isEmpty`, `hasNext`, `hasPrev`).

## Person Class (`Person.java`):
- **Represents a person** with `id`, `firstName`, and `lastName`.
- **Overrides**:
  - `equals` and `hashCode` for correct comparison and hashing.
  - `toString` for a readable string representation.

## Hash Table Tests (`HashTableTest.java`):
- **Comprehensive unit tests** for the hash table implementation.
- **Key Tests**:
  - Adding and checking for elements.
  - Removing elements.
  - Clearing the hash table.
  - Validating empty and non-empty states.
