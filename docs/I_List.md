# I_List Interface

## Definition

|             |                                 |
| ----------- | ------------------------------- |
| Namespace   | mobject-collections             |
| Library     | mobject-collections             |
| Inheritance | [I_Collection](I_Collection.md) |
| Implements  |                                 |

## Remarks

The I_List interface contains common methods and properties found in a list.

## Methods

### GetIndexOf(Item)

Returns the index of an item in a list.

#### Parameters

| Parameters | Datatype | Description                      |
| ---------- | -------- | -------------------------------- |
| Item       | ANY      | The item used to find the index. |

#### Return

| Datatype | Description                                                                   |
| -------- | ----------------------------------------------------------------------------- |
| DINT     | Returns the index of the item if contained in the list, otherwise returns -1. |

### TrimExcess(Item)

Releases any spare capacity in the list

#### Parameters

N/A

#### Return

N/A

### TryGetByIndex(Index, Destination)

Attempts to retrieve the data from the item and copy it to the destination. Only destinations of the correct size can be used.

#### Parameters

| Parameters  | Datatype | Description                                            |
| ----------- | -------- | ------------------------------------------------------ |
| Index       | DINT     | The index of the item to be removed from the list.     |
| Destination | ANY      | The variable to be used as the destination of the copy |

#### Return

| Datatype | Description                                                                                                                                                    |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BOOL     | The method will return TRUE if the copy was completed. FALSE will be returned if the index was not found or the size of the destination was the incorrect size |

### TryGetToByIndex(Index, Destination, DestinationSize)

Attempts to retrieve the data from the item and copy it to the destination. Only destinations of the correct size can be used.

#### Parameters

| Parameters         | Datatype | Description                                                      |
| ------------------ | -------- | ---------------------------------------------------------------- |
| Index              | DINT     | The index of the item to be removed from the list.               |
| DestinationAddress | PVOID    | The variable's address to be used as the destination of the copy |
| DestinationSize    | UDINT    | The variable's size to be used as the destination of the copy    |

#### Return

| Datatype | Description                                                                                                                                                    |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BOOL     | The method will return TRUE if the copy was completed. FALSE will be returned if the index was not found or the size of the destination was the incorrect size |

### TryInsert(Index, Item)

Inserts an item at a specified index. The index must be greater than 0 and less than list item count.

#### Parameters

| Parameters | Datatype | Description                               |
| ---------- | -------- | ----------------------------------------- |
| Index      | DINT     | The index in the list to insert the item. |
| Item       | ANY      | The item to be inserted.                  |

#### Return

| Datatype | Description                                                                                           |
| -------- | ----------------------------------------------------------------------------------------------------- |
| BOOL     | The method will return TRUE if the insert was completed. FALSE will be returned if the method failed. |

### TryRemoveAt(Item)

Removes item from the list using the index. Lists are zero based index.

#### Parameters

| Parameters | Datatype | Description                                        |
| ---------- | -------- | -------------------------------------------------- |
| Index      | DINT     | The index of the item to be removed from the list. |

#### Return

| Datatype | Description                                                                                                |
| -------- | ---------------------------------------------------------------------------------------------------------- |
| BOOL     | The method will return TRUE if the remove was completed. FALSE will be returned if the index was not found |

## Properties

### Capacity

Gets or sets the total number of elements the internal data structure can hold without resizing. It is not possible to set the Capacity lower than 0, or less than the current Count.

The list will start with a capacity of 0. AddItem will automatically increase the capacity to 4. If more space is required to perform AddItem or Insert then the current capacity will be doubled.

#### GET / SET

| Datatype | Description                                                                         |
| -------- | ----------------------------------------------------------------------------------- |
| DINT     | The total number of elements the internal data structure can hold without resizing. |
