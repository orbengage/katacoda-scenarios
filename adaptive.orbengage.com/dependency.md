# Dependency

Dependencies need to be managed. 
There are different types of dependencies such as first party dependencies within the same code. Then there are dependencies within its runtime and third party dependencies which are libraries that we use.

There are dependencies in the method level all the way to system level.

What is a dependency?

A dependency in software exist when one entity needs another to function or complete its scope of work. An entity can be a method or a function or a system. A depends on B imply that A cannot complete its work without B. However B is not dependent on A. It can complete its work without A. 
Entity B may have its own dependencies. Thus there is a dependency chain.

* First party dependencies
* Framework or runtime dependencies
* Third pary dependencies

Why do we need dependency?

A dependency is an abstraction that you do not need to worry about. You do not need to know the implementation or internal details. You just need to know how to use it. So this the code that you do not need to write. This is the case with third party or framework dependencies. 

For the dependencies within your codebase, you do not need to understand the internal working of the code when you are workig on the code tha uses the dependency. Understanding is everything in software. Writing software is all mental work. When you are working on a piece of code, simplicity and hence understandability is supreme. 

What are the important principles in using dependencies?


