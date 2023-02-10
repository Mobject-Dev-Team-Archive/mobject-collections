<p align="center">
  <img width="460" height="300" src="./images/logo.svg">
</p>

> A framework and guide for writing object oriented programs in structured text.

## Opening Statement

A sprinkling of OOP is usually enough to simplify and unclutter procedural code. However, the more you apply OOP, the more you find the need to expand it's scope to accommodate functionality which is missing from the language. For example, writing a simple flashing light class will require its instance to be cyclically called in order for it to update it's hardware output. If you pass this light in to another object then the responsibility of who should cyclic call it becomes hard to reason about. Hence, mobject was conceived. It a framework, library and mindset of how problems such as this can be resolved using both pre-written code and examples.

mobjects' goal is to be a lightweight solution to typical oop problems. Where possible it will allow for both inheritance and composition. I would recommend for you to use inheritance when getting started with the framework, then as you become confident I would recommend that you create objects using composition as this will give you the best chance of code reuse going forwards.
