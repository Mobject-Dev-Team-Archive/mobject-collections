# Queue Class

## Definition

|             |                                                                            |
| ----------- | -------------------------------------------------------------------------- |
| Namespace   | mobject-collections                                                        |
| Library     | mobject-collections                                                        |
| Inheritance | [Disposable](https://benhar-dev.github.io/mobject-disposable/#/disposable) |
| Implements  |                                                                            |

## Remarks

The Queue Class is a general-purpose first in, first out, queue (FIFO). It supports enumerators and implements the GetEnumerator method, consistent with other collection classes in the mobject-collections library.

## Example

```declaration
PROGRAM Main
VAR
	myQueue : Queue;
	value1 : INT := 123;
	value2 : INT := 456;
	value3 : INT := 789;
END_VAR
```

```body

// using Enqueue, TryPeek and TryDequeue
// -------------------------------------

myQueue.Enqueue(value1); // (first->) 123
myQueue.Enqueue(value2); // (first->) 123, 456
myQueue.Enqueue(value3); // (first->) 123, 456, 789

// TryPeek will not remove the item from the queue
allowed := myQueue.TryPeek(output); // allowed = true, output = 123

// TryDequeue will remove the item from the queue
allowed := myQueue.TryDequeue(output); // allowed = true, output = 123
allowed := myQueue.TryDequeue(output); // allowed = true, output = 456
allowed := myQueue.TryDequeue(output); // allowed = true, output = 789

```

Documentation in progress...
