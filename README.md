# Assignment 3 - Bridge Pattern

## Course
Software Design Patterns

## Student
Yerkenkyzy Aruzhan

## Group
SE-2502

## Topic
Bridge Design Pattern - Shape and Renderer

## Description
This project demonstrates the implementation of the Bridge structural design pattern in Java.

The system separates two independent hierarchies:

### Abstraction hierarchy
- `Shape`
- `Circle`
- `Square`

### Implementation hierarchy
- `Renderer`
- `VectorRenderer`
- `RasterRenderer`

The `Shape` abstraction stores a reference to the `Renderer` interface using composition.

This allows shapes and rendering implementations to vary independently.

For example:
- A `Circle` can be rendered using `VectorRenderer`
- The same `Circle` can later switch to `RasterRenderer`
- A `Square` can also use either renderer

The renderer can be changed at runtime without modifying the shape abstraction.

---

## Bridge Pattern Structure

### Abstraction
`Shape`

### Refined Abstractions
- `Circle`
- `Square`

### Implementor
`Renderer`

### Concrete Implementors
- `VectorRenderer`
- `RasterRenderer`

### Client
`Main`

The key part of the Bridge pattern is the relationship between `Shape` and `Renderer`.

```java
protected Renderer renderer;
