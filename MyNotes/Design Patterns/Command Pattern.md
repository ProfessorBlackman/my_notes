The Command Design Pattern is a behavioral design pattern that turns a request into a stand-alone object that contains all information about the request. This transformation allows parameterization of methods with different requests, delay or queue a request's execution, and support undoable operations. Essentially, the Command pattern allows for the decoupling of the object that invokes the operation from the one that knows how to perform it.

### Key Concepts

1. **Command**: An interface that declares a method for executing a command.
2. **Concrete Command**: Implements the Command interface and defines the binding between a Receiver object and an action.
3. **Receiver**: Knows how to perform the operations associated with carrying out a request. Any class can serve as a Receiver.
4. **Invoker**: Asks the command to carry out the request.
5. **Client**: Creates a ConcreteCommand object and sets its receiver.

### Advantages

- **Separation of Concerns**: Decouples the classes that invoke the operation from the object that knows how to execute the operation.
- **Extension**: New commands can be added without changing existing code, which follows the Open-Closed Principle.
- **Composition**: Commands can be composed into macros to perform complex operations.

### Use Cases

- When you need to parameterize objects according to an action to perform.
- When you need to specify, queue, and execute requests at different times.
- When you need to support rollback, logging, or transactional operations.

### Example: Command Pattern in Java

Let's illustrate the Command Pattern with a simple example: a remote control (Invoker) that can turn a light on and off (Receiver).

#### Command Interface

```java
public interface Command {
    void execute();
}
```

#### Concrete Commands

```java
// Turns the light on
class LightOnCommand implements Command {
    private Light light;

    public LightOnCommand(Light light) {
        this.light = light;
    }

    public void execute() {
        light.on();
    }
}

// Turns the light off
class LightOffCommand implements Command {
    private Light light;

    public LightOffCommand(Light light) {
        this.light = light;
    }

    public void execute() {
        light.off();
    }
}
```

#### Receiver

```java
// Receiver class
class Light {
    public void on() {
        System.out.println("Light is on");
    }

    public void off() {
        System.out.println("Light is off");
    }
}
```

#### Invoker

```java
// Invoker
class SimpleRemoteControl {
    private Command slot;

    public void setCommand(Command command) {
        this.slot = command;
    }

    public void buttonWasPressed() {
        slot.execute();
    }
}
```

#### Client

```java
public class RemoteControlTest {
    public static void main(String[] args) {
        SimpleRemoteControl remote = new SimpleRemoteControl();
        Light light = new Light();
        LightOnCommand lightOn = new LightOnCommand(light);
        LightOffCommand lightOff = new LightOffCommand(light);

        // Turn the light on
        remote.setCommand(lightOn);
        remote.buttonWasPressed();

        // Turn the light off
        remote.setCommand(lightOff);
        remote.buttonWasPressed();
    }
}
```

This example demonstrates how the Command pattern enables the `SimpleRemoteControl` class (Invoker) to issue requests to the `Light` class (Receiver) without knowing anything about the operation being performed. The `LightOnCommand` and `LightOffCommand` classes encapsulate the action and the receiver, enabling the `execute` method to have all the information needed to perform the action.