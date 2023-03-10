# I_LinkedListChangedEvent Interface

## Definition

|             |                                                                  |
| ----------- | ---------------------------------------------------------------- |
| Namespace   | mobject-collections                                              |
| Library     | mobject-collections                                              |
| Inheritance | [I_Event](https://benhar-dev.github.io/mobject-events/#/i-event) |
| Implements  |                                                                  |

## Remarks

The I_LinkedListChangedEvent is an event emitted by the [LinkedList](linkedlist.md) class.

## Example

```declaration
FUNCTION_BLOCK MyHandler IMPLEMENTS I_EventHandler
VAR
END_VAR
```

```body
//... no code should go here.
```

```declaration
METHOD HandleEvent
VAR_INPUT
    Event : I_Event;
END_VAR
VAR
    linkedListChangedEvent : I_LinkedListChangedEvent;
    originator : I_LinkedList;
END_VAR
```

```body
IF __QUERYINTERFACE(Event, linkedListChangedEvent) THEN
    // the received event was I_LinkedListChangedEvent.  You can now use the interface
    // to extract which linked list raised it
    // ...
    originator := linkedListChangedEvent.TargetLinkedList;
END_IF

// other event checks can follow here..
// ...
```

## Properties

### TargetLinkedList

Returns the linked list who raised the event.

#### Return

| Datatype                        | Description                          |
| ------------------------------- | ------------------------------------ |
| [I_LinkedList](i-linkedlist.md) | The linked list who raised the event |
