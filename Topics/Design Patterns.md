There are three types:
1. Creational: For class instantiation
2. Structural: Increases functionality of a class without changing much of it's composition
3. Bahavioral: Hoe classes communicate with each other

## Creational Patterns
### Singleton Pattern:
- Create only one instance of the class.
- Provide only one global access point to that object.
- It always includes
		- a static getInstance method to get the object.
	   - a private static variable, holding the only instance of the class
	   - a private constructor, so it can't be instantiated anywhere else.

- types are:
	- Eager Instantiation:
		```java
		public class EagerSingleton {
			// create an instance of the class.
				private static EagerSingleton instance = new EagerSingleton();
			
		// private constructor, so it cannot be instantiated outside this class.
				private EagerSingleton() {  }
			
				// get the only instance of the object created.
				public static EagerSingleton getInstance() {
					return instance;
				}
		}
```

