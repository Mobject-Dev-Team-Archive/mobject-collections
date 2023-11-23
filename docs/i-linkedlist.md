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

Add an item to the linked list after a given node.

#### Parameters

| Parameters | Datatype                                | Description                                           |
| ---------- | --------------------------------------- | ----------------------------------------------------- |
| After      | [I_LinkedListNode](i-linkedlistnode.md) | The node object which the value will be placed after. |
| Value      | ANY                                     | The value to store in the linked list.                |

#### Return

N/A

### AddBefore(Before, Value)

Add an item to the linked list before a given node.

#### Parameters

| Parameters | Datatype                                | Description                                            |
| ---------- | --------------------------------------- | ------------------------------------------------------ | --- |
| Before     | [I_LinkedListNode](i-linkedlistnode.md) | The node object which the value will be placed before. |
| Value      | ANY                                     | The value to store in the linked list.                 |     |

#### Return

N/A

### AddFirst(Value)

Add an item to the start of the linked list.

#### Parameters

| Parameters | Datatype | Description                            |
| ---------- | -------- | -------------------------------------- |
| Value      | ANY      | The value to store in the linked list. |

#### Return

N/A

### AddLast(Value)

Add an item to the end of the linked list.

#### Parameters

| Parameters | Datatype | Description                            |
| ---------- | -------- | -------------------------------------- |
| Value      | ANY      | The value to store in the linked list. |

#### Return

N/A

### Find(Value)

Returns the first I_LinkedListNode which matches the value supplied.

#### Parameters

| Parameters | Datatype | Description             |
| ---------- | -------- | ----------------------- |
| Value      | ANY      | The value to search for |

#### Return

| Datatype                                | Description                                                                  |
| --------------------------------------- | ---------------------------------------------------------------------------- |
| [I_LinkedListNode](i-linkedlistnode.md) | The method will return the first matching node, or zero if no value is found |

### FindLast(Value)

Returns the last I_LinkedListNode which matches the value supplied.

#### Parameters

| Parameters | Datatype | Description             |
| ---------- | -------- | ----------------------- |
| Value      | ANY      | The value to search for |

#### Return

| Datatype                                | Description                                                                 |
| --------------------------------------- | --------------------------------------------------------------------------- |
| [I_LinkedListNode](i-linkedlistnode.md) | The method will return the last matching node, or zero if no value is found |

### Remove(Value)

Removes the first matching value from the linked list

#### Parameters

| Parameters | Datatype | Description                                   |
| ---------- | -------- | --------------------------------------------- |
| Value      | ANY      | The value to be removed from the linked list. |

#### Return

N/A

### RemoveFirst()

Removes the first item from the linked list

#### Parameters

N/A

#### Return

N/A

### RemoveLast()

Removes the last item from the linked list

#### Parameters

N/A

#### Return

N/A

## Properties

### First

Returns the first node in the linked list.

#### Return

| Datatype         | Description                       |
| ---------------- | --------------------------------- |
| I_LinkedListNode | The first node in the linked list |

### Last

Returns the last node in the linked list.

#### Return

| Datatype         | Description                      |
| ---------------- | -------------------------------- |
| I_LinkedListNode | The last node in the linked list |
