## Definition:
**Design patterns** are typical solutions to common problems in software design. Each pattern is like a blueprint that you can customize to solve a particular design problem in your code.
- **History**: 
	- Patterns are solutions to frequently occurring problems. So when the problems are recurring, at some point someone will document the solution and it will be generalized so it can be implemented to solve similar problems in the future; ergo a new design pattern
	- [History of patterns](https://refactoring.guru/design-patterns/history)
- **Criticism**:
	- **The need for design patterns can signify a weak programming language:** Usually the need for patterns arises when people choose a programming language or a technology that lacks the necessary level of abstraction. In this case, patterns become a kludge that gives the language much-needed super-abilities. For example, the [Strategy](https://refactoring.guru/design-patterns/strategy) pattern can be implemented with a simple anonymous (lambda) function in most modern programming languages.
	- **Inefficient Solutions:** 
		Patterns try to systematize approaches that are widely used. This becomes viewed as a dogma, or the go to approach for some problems. This means some devs would implement these patterns to the letter without adapting them or considering the context of their project.
	- **Unjustified use:**
		>If all you have is a hammer, everything looks like a nail.
		
		Novices who have just learnt design patterns tend to try to apply them everywhere, even when a simpler code would do just fine or might just be better.
		
## Creational Patterns
- provide object creation mechanisms that increase flexibility and reuse of existing code.
- **Factory Method:**
	- Defines an interface for creating objects but lets subclasses decide which class to instantiate.
	- Promotes loose coupling and allows for dynamic object creation based on context.
- **Builder Pattern:**
	- Separates the object construction process into steps, making the process flexible and allowing for method chaining.
- **Singleton Pattern:**
	- Allows only a single instance of the class to exist.
	- Very useful for configurations, logging, or resource management
- **Prototype Pattern:**
	-  The Prototype pattern allows us to create new objects by copying an existing instance (the prototype). Instead of creating fresh objects, we clone the prototypical instance.
## **Structural patterns**:
- explain how to assemble objects and classes into larger structures, while keeping these structures flexible and efficient.
- **Adapter Pattern:**
	- Allows incompatible interfaces to work together by converting the interface of one class to the other.
- **Decorator Pattern:**
	- Attaches responsibilities to an object, as a flexible alternative to subclassing
- **[[Facade Pattern]]:**
	- This pattern hides the complexity of a class, library, or framework. It offers a simpler interface to this framework. So it's kinda like abstraction. Essentially it acts like a high-level interface that makes the subsystems easier to use.
## Behavioral patterns:
- take care of effective communication and the assignment of responsibilities between objects. 
- **[[Observer Pattern]]:**
	- Allows an object to maintain a list of it's dependents (observers), and notify them automatically of any changes.
	- It's foundational for event-driven systems and is extensively used to implement distributed event-handling, such as mvc architecture.
	- So yea, when using a state management tool like Provider or riverpod in flutter, this pattern is being used. Also when using spring events or Django signals, this is being used.
- **[[Strategy pattern]]:**
	- is a behavioral design pattern that lets you define a family of algorithms, put each of them into a separate class, and make their objects interchangeable.
- **[[Command Pattern]]:**
	- 