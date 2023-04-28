# I_Collection Interface

## Definition

|             |                                                                                                                                                                                           |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Namespace   | mobject-collections                                                                                                                                                                       |
| Library     | mobject-collections                                                                                                                                                                       |
| Inheritance | [I_Enumerable](http://enumerable.mobject.org/#/i-enumerable), [I_Disposable](http://disposable.mobject.org/#/i-disposable), [I_EventEmitter](http://events.mobject.org/#/i-event-emitter) |
| Implements  |                                                                                                                                                                                           |

## Remarks

The I_Collection interface contains common methods and properties found in a collection.

## Methods

### AddItem(Item)

Add an item to the collection.

#### Parameters

| Parameters | Datatype | Description                          |
| ---------- | -------- | ------------------------------------ |
| Item       | ANY      | The item to store in the collection. |

#### Return

N/A

### Clear()

Removes all items from the collection.

#### Parameters

N/A

#### Return

N/A

### Contains(Item)

Checks to see if an item is contained in the collection.

#### Parameters

| Parameters | Datatype | Description                            |
| ---------- | -------- | -------------------------------------- |
| Item       | ANY      | The item used to check the collection. |

#### Return

| Datatype | Description                                             |
| -------- | ------------------------------------------------------- |
| BOOL     | Returns true if the item is contained in the collection |

### CopyTo(Destination)

Copies the contents of the collection to an array. The array must be of the correct size to contain all of the items.

#### Parameters

| Parameters  | Datatype | Description                                 |
| ----------- | -------- | ------------------------------------------- |
| Destination | ANY      | The array which will act as the destination |

#### Return

| Datatype | Description                                                                                                                   |
| -------- | ----------------------------------------------------------------------------------------------------------------------------- |
| BOOL     | The method will return TRUE if the copy was completed. FALSE will be returned if the destination size is too big or too small |

### CopyToLocation(Destination)

Copies the contents of the collection to an array defined by address and size. The array must be of the correct size to contain all of the items.

#### Parameters

| Parameters         | Datatype | Description                                                |
| ------------------ | -------- | ---------------------------------------------------------- |
| DestinationAddress | PVOID    | The address of the array which will act as the destination |
| DestinationSize    | UDINT    | The size of the array which will act as the destination    |

#### Return

| Datatype | Description                                                                                                                   |
| -------- | ----------------------------------------------------------------------------------------------------------------------------- |
| BOOL     | The method will return TRUE if the copy was completed. FALSE will be returned if the destination size is too big or too small |

### RemoveItem(Item)

Removes the first matching item from the collection.

#### Parameters

| Parameters | Datatype | Description                                 |
| ---------- | -------- | ------------------------------------------- |
| Item       | ANY      | The item to be removed from the collection. |

#### Return

N/A

## Properties

### Count

Returns the total number of items held in the collection

#### Return

| Datatype | Description                   |
| -------- | ----------------------------- |
| DINT     | Total items in the collection |
