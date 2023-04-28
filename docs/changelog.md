# Changelog

# 0.7.0

- Added List and ListForwardEnumerator Classes.
- Changed I_Collection to extend from I_EventEmitter.

!> This update contains the following breaking changes.

- I_Collection.Count is now DINT.
- Individual OnChanged and OnDisposed event classes have been removed and replaced by generic collection events.
- Added mobject-enumerable 0.1.0.
- Changed all Destination to DestinationAddress on arguments of PVOID.

# 0.6.0

- Library built using 4024.44.
- Queue and Stack support events 'OnChanged' and 'OnDisposed'.

!> This update contains the following breaking changes.

- LinkedListNode methods Get and GetTo have been renamed to TryGet and TryGetTo.
- LinkedList events 'OnLinkedListChanged' and 'OnLinkedListDisposed' renamed to 'OnChanged' and 'OnDisposed'. This will allow all collections to use the same name and for the event emitter to move to the I_Collection interface on a future release.
- Removed Collection but kept I_Collection

# 0.5.0

- Added Collection
- Added further tests for collection and enumerators

# 0.4.0

- Remove I_Enumerable interface to mobject-enumerable
- Added mobject-enumerable 0.0.0

# 0.3.0

- Added I_Enumerable interface
- Added I_Collection interface
- Added I_Queue interface
- Added I_Stack interface

## 0.2.1

- Updated to support mobject-disposable v0.3.1-alpha
- Updated to support mobject-events v0.4.1-alpha

## 0.2.0

- Updated to support mobject-disposable v0.3.0-alpha
- Updated to support mobject-events v0.4.0-alpha
- Added tests for enumerators
- All tests now passing

## 0.1.0

### Queue

- Added support for CopyTo and CopyToLocation, which matches the feature on LinkedList.

### NEW - Stack

- Added the Stack (fifo) class.

## 0.0.0

- Initial commit
- Supports LinkedList, ForwardEnumerators, Queue's.
