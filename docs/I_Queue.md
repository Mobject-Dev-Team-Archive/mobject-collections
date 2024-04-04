# I_Queue Interface

## Definition

|             |                                 |
| ----------- | ------------------------------- |
| Namespace   | mobject-collections             |
| Library     | mobject-collections             |
| Inheritance | [I_Collection](I_Collection.md) |
| Implements  |                                 |

## Remarks

The I_Queue interface provides a standardized approach to queue data structure management in the mobject-collections library. It extends the functionality of the [I_Collection](I_Collection.md) interface, focusing on FIFO (First-In-First-Out) operations commonly associated with queues. This interface is particularly useful in scenarios where orderly processing of items is required.

## Methods

### Enqueue(Item)

Enqueues an item, adding it to the back of the queue. This operation is typically used for inserting new data elements into the queue.

#### Parameters

| Parameters | Datatype | Description                               |
| ---------- | -------- | ----------------------------------------- |
| Item       | ANY      | The item to add to the back of the queue. |

#### Return

N/A

### TryDequeue(Destination)

Attempts to dequeue an item from the front of the queue. If successful, the item is removed from the queue and stored in the 'Destination' parameter, and the method returns TRUE.

#### Parameters

| Parameters  | Datatype | Description                          |
| ----------- | -------- | ------------------------------------ |
| Destination | ANY      | A symbol to store the dequeued item. |

#### Return

| Datatype | Description                                              |
| -------- | -------------------------------------------------------- |
| BOOL     | Returns TRUE if dequeue was successful, FALSE otherwise. |

### TryPeek(Destination)

Attempts to view the item at the front of the queue without removing it. If successful, the item is copied to the 'Destination' parameter, and the method returns TRUE.

#### Parameters

| Parameters  | Datatype | Description                                           |
| ----------- | -------- | ----------------------------------------------------- |
| Destination | ANY      | A symbol to store the item at the front of the queue. |

#### Return

| Datatype | Description                                                |
| -------- | ---------------------------------------------------------- |
| BOOL     | Returns TRUE if the item could be viewed, FALSE otherwise. |
