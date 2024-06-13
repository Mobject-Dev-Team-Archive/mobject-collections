# Changelog

## v1.3.0-beta

- Updated to support mobject-disposable v1.1.1
- Updated to support mobject-enumerable v1.2.0
- Updated to support mobject-events v1.1.0

## v1.2.0-beta

- Added OrderedDictionary, which preserves the order of added items when using enumerators
- Added IsEmpty to I_Collection

## v1.1.0-beta

- Updated to support mobject-enumerable v1.1.0-beta.
- Added the Reset method.
- Dictionary to support I_KeyValueEnumerable.
- Dictionary enumerator to support I_KeyValueForwardEnumerator.
- Enumerators will auto dispose on parent dispose.

## v1.0.0-beta

- Changed status from alpha to beta.
- Updated documentation to support dark mode.
- Library built using 4024.53.
- Updated to support mobject-disposable v1.0.0-beta.
- Updated to support mobject-enumerable v1.0.0-beta.
- Updated to support mobject-events v1.0.0-beta.
- Documentation correction.

# v0.9.0-alpha

- Documentation update

!> This update contains the following breaking changes.

- Method calls which perform an action and return TRUE or FALSE based on their success are now prefixed with "Try". For example, list.CopyTo() -> list.TryCopyTo(). This is to improve their readability and promote their use in IF statements.

# v0.8.1-alpha

- Bugfix Dictionary ForwardEnumerator not returning correct element when MoveNext() was called.
- Library built using 4024.53.

# v0.8.0-alpha

- Added Dictionary Class.
- Bugfix Events were not implemented correctly on the ListEnumerator. These have been added.
- Converted referenced libraries to actual libraries rather than placeholders
- Added I_CollectionNode as a base to I_LinkedListNode, I_ListNode and I_DictionaryNode.

!> This update contains the following breaking changes.

- Removed Reset from enumerators (as this is not a commonly implemented method)
- FB_init of ListForwardEnumerator has argument List changed to Parent.

# v0.7.0-alpha

- Added List and ListForwardEnumerator Classes.
- Changed I_Collection to extend from I_EventEmitter.

!> This update contains the following breaking changes.

- I_Collection.Count is now DINT.
- Individual OnChanged and OnDisposed event classes have been removed and replaced by generic collection events.
- Added mobject-enumerable 0.1.0.
- Changed all Destination to DestinationAddress on arguments of PVOID.

# v0.6.0-alpha

- Library built using 4024.44.
- Queue and Stack support events 'OnChanged' and 'OnDisposed'.

!> This update contains the following breaking changes.

- LinkedListNode methods Get and GetTo have been renamed to TryGet and TryGetTo.
- LinkedList events 'OnLinkedListChanged' and 'OnLinkedListDisposed' renamed to 'OnChanged' and 'OnDisposed'. This will allow all collections to use the same name and for the event emitter to move to the I_Collection interface on a future release.
- Removed Collection but kept I_Collection

# v0.5.0-alpha

- Added Collection
- Added further tests for collection and enumerators

# v0.4.0-alpha

- Remove I_Enumerable interface to mobject-enumerable
- Added mobject-enumerable 0.0.0

# v0.3.0-alpha

- Added I_Enumerable interface
- Added I_Collection interface
- Added I_Queue interface
- Added I_Stack interface

## v0.2.1-alpha

- Updated to support mobject-disposable v0.3.1-alpha
- Updated to support mobject-events v0.4.1-alpha

## v0.2.0-alpha

- Updated to support mobject-disposable v0.3.0-alpha
- Updated to support mobject-events v0.4.0-alpha
- Added tests for enumerators
- All tests now passing

## v0.1.0-alpha

### Queue

- Added support for CopyTo and CopyToLocation, which matches the feature on LinkedList.

### NEW - Stack

- Added the Stack (fifo) class.

## v0.0.0-alpha

- Initial commit
- Supports LinkedList, ForwardEnumerators, Queue's.
