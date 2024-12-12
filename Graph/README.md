# Overview
This repository provides an implementation of a **Graph** data structure in Java. It supports generic vertices and edge labels, with extensions for weighted edges and specific use cases such as friendships. The repository includes:

- **`IGraph.java`** - Interface defining graph operations.
- **`Graph.java`** - Implementation of the generic graph.
- **`Person.java`** - Represents a person with attributes.
- **`Friendship.java`** - Represents a friendship.
- **`Weighted.java`** - Interface for weighted objects.
- **`WeightedFriendship.java`** - Represents a friendship with a weight.
- **`GraphTest.java`** - Unit tests for the graph implementation.

# Features

## Graph Interface (`IGraph.java`):
- **Key Methods**:
  - `add(V v)`: Adds a new vertex.
  - `getEdge(V u, V v)`: Retrieves the label of the edge between two vertices.
  - `putEdge(V u, V v, E edgeLabel)`: Adds or updates an edge between two vertices.
  - `containsVertex(V v)`: Checks if the graph contains a specific vertex.
  - `removeVertex(V v)`: Removes a vertex and its associated edges.
  - `removeEdge(V u, V v)`: Removes the edge between two vertices.
  - `getWeight(V u, V v)`: Returns the weight of an edge if it exists.
  - `toString()`: Lists all vertices.
  - `toStringExtended()`: Lists vertices with their edges.
  - `areAdjacent(V u, V v)`: Checks if two vertices are adjacent.

## Graph Implementation (`Graph.java`):
- **Implements the `IGraph` interface**.
- **Key Features**:
  - Uses a map to store vertices and their adjacency lists.
  - Supports bidirectional edges.
  - Handles weighted edges using the `Weighted` interface or numeric labels.
- **Inner Class `Edge`**:
  - Encapsulates an edge's endpoints, label, and weight.
  - Supports comparison and string representation.

## Person Class (`Person.java`):
- Represents a person with `id`, `firstName`, and `lastName`.
- Implements **`Comparable`** and overrides `equals`, `hashCode`, and `toString` for usability in graphs.

## Friendship and WeightedFriendship:
- **`Friendship.java`**:
  - Encapsulates a friendship with a start date.
- **`WeightedFriendship.java`**:
  - Extends `Friendship` with a weight (e.g., strength of the relationship).

## Weighted Interface (`Weighted.java`):
- Defines a `getWeight()` method for weighted objects.

## Graph Tests (`GraphTest.java`):
- **Comprehensive unit tests** for graph functionality.
- **Key Tests**:
  - Vertex addition and removal.
  - Edge addition, removal, and weight retrieval.
  - Adjacency checks and edge retrieval.
  - Extended scenarios using `Person`, `Friendship`, and `WeightedFriendship`.
