# I_LinkedList Interface

## Definition

|             |                                 |
| ----------- | ------------------------------- |
| Namespace   | mobject-collections             |
| Library     | mobject-collections             |
| Inheritance | [I_Collection](i-collection.md) |
| Implements  |                                 |

## Remarks

The I_LinkedList interface contains common methods and properties found on a basic implementation of a linked list.

## Methods

### AddAfter(After, Value)

#### Parameters

| Parameters | Datatype                                |
| ---------- | --------------------------------------- |
| After      | [I_LinkedListNode](i-linkedlistnode.md) |
| Value      | ANY                                     |

#### Return

N/A

### AddBefore(Before, Value)

#### Parameters

| Parameters | Datatype                                |
| ---------- | --------------------------------------- |
| Before     | [I_LinkedListNode](i-linkedlistnode.md) |
| Value      | ANY                                     |

#### Return

N/A

### AddFirst(Value)

#### Parameters

| Parameters | Datatype |
| ---------- | -------- |
| Value      | ANY      |

#### Return

N/A

### AddLast(Value)

#### Parameters

| Parameters | Datatype |
| ---------- | -------- |
| Value      | ANY      |

#### Return

N/A

### Find(Value)

#### Parameters

| Parameters | Datatype |
| ---------- | -------- |
| Value      | ANY      |

#### Return

| Datatype                                |
| --------------------------------------- |
| [I_LinkedListNode](i-linkedlistnode.md) |

### FindLast(Value)

#### Parameters

| Parameters | Datatype |
| ---------- | -------- |
| Value      | ANY      |

#### Return

| Datatype                                |
| --------------------------------------- |
| [I_LinkedListNode](i-linkedlistnode.md) |

### Remove(Value)

#### Parameters

| Parameters | Datatype |
| ---------- | -------- |
| Value      | ANY      |

#### Return

N/A

### RemoveFirst()

#### Parameters

N/A

#### Return

N/A

### RemoveLast()

#### Parameters

N/A

#### Return

N/A

## Properties

### First

#### Return

| Datatype         |
| ---------------- |
| I_LinkedListNode |

### Last

#### Return

| Datatype         |
| ---------------- |
| I_LinkedListNode |
