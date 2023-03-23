<p align="center">
  <img width="460" src="./images/logo.svg">
</p>

> A framework and guide for writing object oriented programs in structured text.

## The mobject-collections Library

This is one of the many libraries of mobject. This library focuses on dynamic collections.

## What is mobject?

Pronounced mob-ject.

A sprinkling of OOP is usually enough to simplify and unclutter procedural code. However, the more you apply OOP, the more you find the need to expand it's scope to accommodate functionality which is missing from the language. Hence, mobject was conceived. It's a framework, library and mindset of how problems such as this can be resolved using both pre-written code and examples.

mobject's goal is to be a lightweight solution to typical oop problems.

## Why use mobject-collections?

The mobject-collections library provides a set of efficient and flexible data structures that can be used to manage collections of objects in your industrial control system. The library currently includes threr classes: LinkedList Stack and Queue, with Dynamic Array and Dictionary coming soon.

### LinkedList (Double linked list)

<img src="./images/linkedlist-example.svg">

The LinkedList class is a data structure that allows for efficient insertion, deletion, and traversal of items in a collection. Linked lists are particularly useful when you need to insert or delete items frequently. Additionally, linked lists can be easily be converted to static arrays.

Using the LinkedList class can help you to efficiently manage collections of objects in your industrial control system, particularly when frequent insertions and deletions are required.

The image above depicts a double linked list, which it the term given to a linked list who tracks both the head and tail. The benefit of a double linked list is that both forward and backwards traversing is possible.

### Queue

<img src="./images/queue-example.svg">

The Queue class is a data structure that follows the First-In-First-Out (FIFO) principle. Items are added to the back of the queue and removed from the front of the queue, in the order they were added. Queues are particularly useful for managing tasks that need to be processed in the order they were received, such as a set of instructions or a sequence of events.

Using the Queue class can help you to manage your system's tasks in an organized and efficient manner, ensuring that they are processed in the correct order and without any unnecessary delays.

### Stack

<img src="./images/stack-example.svg">

The Stack class is a data structure that follows the Last-In-First-Out (LIFO) principle. Items are added and to the front of the stack and removed from the front of the stack also, in the order they were added. Stacks are particularly useful for managing tasks that need to be processed in the most recent order they were received, such as a set of instructions or a sequence of events.

Using the Stack class can help you to manage your system's tasks in an organized and efficient manner, ensuring that they are processed in the correct order and without any unnecessary delays.

### Dynamic Array and Dictionary

The mobject-collections library will soon be expanding to include additional classes: Dynamic Array and Dictionary. Dynamic arrays are similar to regular arrays, but with the added benefit of being able to dynamically resize themselves as needed. Dictionaries are a data structure that allow for efficient key-value lookups.

With the addition of these classes, the mobject-collections library will provide a comprehensive set of data structures that can be used to manage collections of objects in a wide range of scenarios.
