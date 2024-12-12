# Overview
This repository provides an implementation of a **Stack** using a **Doubly Linked List (DLinkedList)** in Java. It includes a custom stack class, tests for the stack functionality, and a postfix expression evaluator. The repository contains:

- **`Stack.java`** - Interface defining stack operations.
- **`DLinkedList.java`** - Doubly linked list implementation.
- **`DLinkedListStack.java`** - Implements the stack using a doubly linked list.
- **`DLinkedListStackTest.java`** - Unit tests for the `DLinkedListStack`.
- **`EvaluatePostfix.java`** - Evaluates postfix expressions using the stack.

# Features

## Stack Interface (`Stack.java`):
- **Key Methods**:
  - `push(T t)`: Pushes an element onto the stack.
  - `pop()`: Removes and returns the top element from the stack.
  - `top()`: Returns the top element without removing it.
  - `isEmpty()`: Checks if the stack is empty.

## Doubly Linked List (`DLinkedList.java`):
- Implements the `List` interface.
- **Key Features**:
  - Efficient insertion, deletion, and traversal.
  - Maintains references to next and previous nodes for bidirectional traversal.

## DLinkedListStack (`DLinkedListStack.java`):
- Implements the `Stack` interface using a `DLinkedList`.
- **Key Features**:
  - Efficient push and pop operations.
  - Maintains a reference to the top of the stack.
- **Methods**:
  - `push(T t)`: Inserts an element onto the stack and updates the top reference.
  - `pop()`: Removes and returns the top element. Updates the top reference.
  - `top()`: Returns the current top element without modifying the stack.
  - `isEmpty()`: Returns `true` if the stack is empty.
  - `toString()`: Converts the stack into a string representation.

## Stack Tests (`DLinkedListStackTest.java`):
- **Comprehensive unit tests** for stack functionality.
- **Key Tests**:
  - Tests `push`, `pop`, `top`, and `isEmpty` methods.
  - Validates correct handling of edge cases such as empty stacks.
  - Verifies the stack's string representation.

## Postfix Evaluator (`EvaluatePostfix.java`):
- Reads a postfix expression from standard input.
- Uses a `DLinkedListStack` to evaluate the expression.
- **Supported Operations**:
  - Addition (`+`), Subtraction (`-`), Multiplication (`*`), Division (`/`).
- **Error Handling**:
  - Handles invalid expressions gracefully, displaying error messages.
