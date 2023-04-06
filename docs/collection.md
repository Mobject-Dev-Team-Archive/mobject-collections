# Collection Class

## Definition

|             |                                                                                  |
| ----------- | -------------------------------------------------------------------------------- |
| Namespace   | mobject-collections                                                              |
| Library     | mobject-collections                                                              |
| Inheritance | [Disposable](https://mobject-dev-team.github.io/mobject-disposable/#/disposable) |
| Implements  | [I_Collection](i-collection.md)                                                  |

## Remarks

The Collection is a general-purpose data structure.

## Example

```declaration
PROGRAM Main
VAR
	collection : Collection;
	value1 : INT := 123;
	value2 : INT := 456;
	value3 : INT := 789;
	count : ULINT;
	output : INT;
	allowed : BOOL;
END_VAR
```

```body
collection.AddItem(value1);
collection.AddItem(value2);
collection.AddItem(value3);

count := collection.Count; // count = 3;

enumerator := collection.GetEnumerator();
// the enumerator follows the .net style, which means you must call MoveNext once to
// move to the first item.  This allows you to directly use the enumerator in a while
// loop.
WHILE enumerator.MoveNext() DO
	enumerator.TryGet(output);
END_WHILE;
// you must dispose enumerators as they are new objects.
enumerator.Dispose();
```

## Methods

### AddItem(Item)

Add an item to the collection.

#### Parameters

| Parameters | Datatype | Description                          |
| ---------- | -------- | ------------------------------------ |
| Item       | ANY      | The item to store in the collection. |

#### Return

N/A

#### Usage

```declaration
collection : Collection;
value : INT := 123;
```

```body
collection.AddItem(value);
```

### Clear()

Removes all items from the collection.

#### Parameters

N/A

#### Return

N/A

#### Usage

```declaration
collection : Collection;
```

```body
collection.Clear();
```

### Contains(Item)

Checks to see if an item is contained in the collection.

#### Parameters

| Parameters | Datatype | Description                          |
| ---------- | -------- | ------------------------------------ |
| Item       | ANY      | The item to store in the collection. |

#### Return

| Datatype | Description                                             |
| -------- | ------------------------------------------------------- |
| BOOL     | Returns true if the item is contained in the collection |

#### Usage

```declaration
collection : Collection;
value : INT := 123;
result : BOOL;
```

```body
collection.AddItem(value);
result := collection.Contains(value); // result = TRUE
```

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

#### Usage

```declaration
collection : Collection;
value1 : INT := 123;
value2 : INT := 456;
value3 : INT := 789;
myArray : ARRAY [0..2] OF INT;
```

```body
collection.AddItem(value1);
collection.AddItem(value2);
collection.AddItem(value3);
collection.CopyTo(myArray); // myArray = [123,456,789];
```

### CopyToLocation(Destination)

Copies the contents of the collection to an array defined by address and size. The array must be of the correct size to contain all of the items.

#### Parameters

| Parameters      | Datatype | Description                                                |
| --------------- | -------- | ---------------------------------------------------------- |
| Destination     | PVOID    | The address of the array which will act as the destination |
| DestinationSize | UDINT    | The size of the array which will act as the destination    |

#### Return

| Datatype | Description                                                                                                                   |
| -------- | ----------------------------------------------------------------------------------------------------------------------------- |
| BOOL     | The method will return TRUE if the copy was completed. FALSE will be returned if the destination size is too big or too small |

#### Usage

```declaration
collection : Collection;
value1 : INT := 123;
value2 : INT := 456;
value3 : INT := 789;
myArray : ARRAY [0..2] OF INT;
```

```body
collection.AddItem(value1);
collection.AddItem(value2);
collection.AddItem(value3);
collection.CopyToLocation(ADR(myArray),SIZEOF(myArray)); // myArray = [123,456,789];
```

### Dispose()

Will trigger the object for deletion.

#### Parameters

N/A

#### Return

N/A

#### Usage

```example
collection.Dispose()
```

### GetEnumerator()

Returns a forward enumerator for the collection. More information on the enumerators can be found [here](https://mobject-dev-team.github.io/mobject-enumerable/#/i-forward-enumerator)

!> Enumerators are \_\_NEW objects, which means you must dispose of any enumerators you make once you are finished using them. Failure to do so will result in a memory leak.

#### Parameters

N/A

#### Return

| Datatype                                                                                            | Description                                                    |
| --------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| [I_ForwardEnumerator](https://mobject-dev-team.github.io/mobject-enumerable/#/i-forward-enumerator) | The method will return a forward enumerator for the collection |

#### Usage

```declaration
collection : Collection;
value1 : INT := 123;
value2 : INT := 456;
value3 : INT := 789;
output : INT;
enumerator : I_ForwardEnumerator;
```

```body
collection.AddItem(value1);
collection.AddItem(value2);
collection.AddItem(value3);
enumerator := collection.GetEnumerator();

// the enumerator follows the .net style, which means you must call MoveNext once to
// move to the first item.  This allows you to directly use the enumerator in a while
// loop.
WHILE enumerator.MoveNext() DO
	enumerator.TryGet(output); // 1st pass output = 123, 2nd pass output = 456, 3rd pass output = 789
END_WHILE;

// you must dispose enumerators as they are new objects.
enumerator.Dispose();
```

### RemoveItem(Item)

Removes the first matching item from the collection.

#### Parameters

| Parameters | Datatype | Description                                 |
| ---------- | -------- | ------------------------------------------- |
| Item       | ANY      | The item to be removed from the collection. |

#### Return

N/A

#### Usage

```declaration
collection : Collection;
value1 : INT := 123;
value2 : INT := 456;
value3 : INT := 789;
```

```body
collection.AddItem(value1);
collection.AddItem(value2);
collection.AddItem(value3);
collection.RemoveItem(value2); // 123, 789
```

## Properties

### Count

Returns the total number of items held in the collection

#### Return

| Datatype | Description                   |
| -------- | ----------------------------- |
| ULINT    | Total items in the collection |

#### Usage

```declaration
collection : Collection;
value1 : INT := 123;
value2 : INT := 456;
value3 : INT := 789;
count : ULINT;
```

```body
collection.AddItem(value1);
collection.AddItem(value2);
collection.AddItem(value3);
count := collection.Count;
```
