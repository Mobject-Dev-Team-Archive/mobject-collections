# I_Enumerable Interface

## Definition

|             |                            |
| ----------- | -------------------------- |
| Namespace   | mobject-collections        |
| Library     | mobject-collections        |
| Inheritance | \_\_System.IQueryInterface |
| Implements  |                            |

## Remarks

The I_Enumerable interface contains common methods and properties found on objects which are enumerable.

## Methods

### GetEnumerator()

Returns a forward enumerator for the enumerable object. More information on the enumerators can be found [here](i-forwardenumerator.md)

!> Enumerators are \_\_NEW objects, which means you must dispose of any enumerators you make once you are finished using them. Failure to do so will result in a memory leak.

#### Parameters

N/A

#### Return

| Datatype                                      | Description                                                           |
| --------------------------------------------- | --------------------------------------------------------------------- |
| [I_ForwardEnumerator](i-forwardenumerator.md) | The method will return a forward enumerator for the enumerable object |
