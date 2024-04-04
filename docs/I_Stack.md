# I_Stack Interface

## Definition

|             |                                 |
| ----------- | ------------------------------- |
| Namespace   | mobject-collections             |
| Library     | mobject-collections             |
| Inheritance | [I_Collection](I_Collection.md) |
| Implements  |                                 |

## Remarks

The I_Stack interface is part of the mobject-collections library and is designed to facilitate stack data structure management. This interface extends the [I_Collection](I_Collection.md) interface, focusing on LIFO (Last-In-First-Out) operations typical of stacks. It is ideal for scenarios where elements need to be processed in a reversed order compared to their insertion sequence.

## Methods

### Push(Item)

Pushes an item onto the top of the stack.

#### Parameters

| Parameters | Datatype | Description                           |
| ---------- | -------- | ------------------------------------- |
| Item       | ANY      | The item to be pushed onto the stack. |

#### Return

N/A

### TryPeek(Destination)

Attempts to view the item at the top of the stack without removing it.

#### Parameters

| Parameters  | Datatype | Description                                         |
| ----------- | -------- | --------------------------------------------------- |
| Destination | ANY      | A symbol to store the item at the top of the stack. |

#### Return

| Datatype | Description                                                |
| -------- | ---------------------------------------------------------- |
| BOOL     | Returns TRUE if the item could be viewed, FALSE otherwise. |

### TryPop(Destination)

Attempts to remove the item at the top of the stack.

#### Parameters

| Parameters  | Datatype | Description                                            |
| ----------- | -------- | ------------------------------------------------------ |
| Destination | ANY      | A symbol to store the item being popped off the stack. |

#### Return

| Datatype | Description                                                        |
| -------- | ------------------------------------------------------------------ |
| BOOL     | Returns TRUE if the pop operation was successful, FALSE otherwise. |
