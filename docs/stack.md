# Stack Class

## Definition

|             |                                                          |
| ----------- | -------------------------------------------------------- |
| Namespace   | mobject-collections                                      |
| Library     | mobject-collections                                      |
| Inheritance | [Disposable](http://disposable.mobject.org/#/disposable) |
| Implements  | [I_Queue](i-stack.md)                                    |

## Remarks

The Stack class is a data structure that follows the Last-In-First-Out (LIFO) principle. Items are added and to the front of the stack and removed from the front of the stack also, in the order they were added. Stacks are particularly useful for managing tasks that need to be processed in the most recent order they were received, such as a set of instructions or a sequence of events.

<img src="./images/stack-example.svg">

## Example

```declaration
PROGRAM Main
VAR
	stack : Stack;
	value1 : INT := 123;
	value2 : INT := 456;
	value3 : INT := 789;
	output : INT;
	allowed : BOOL;
END_VAR
```

```body
// using Push, TryPeek and TryPop
// -------------------------------------

stack.Push(value1); // (fifo->) 123
stack.Push(value2); // (fifo->) 456, 123
stack.Push(value3); // (fifo->) 789, 456, 123

// TryPeek will not remove the item from the stack
allowed := stack.TryPeek(output); // allowed = true, output = 789

// TryDequeue will remove the item from the queue
allowed := stack.TryPop(output); // allowed = true, output = 789
allowed := stack.TryPop(output); // allowed = true, output = 456
allowed := stack.TryPop(output); // allowed = true, output = 123

```

Documentation in progress...
