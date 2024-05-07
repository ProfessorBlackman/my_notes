The Observer Pattern is a behavioral design pattern that allows an object, known as the subject, to maintain a list of its dependents, called observers, and notify them automatically of any state changes, usually by calling one of their methods. It's a foundational pattern for event-driven systems and is extensively used in implementing distributed event handling systems, such as the model-view-controller (MVC) architectural pattern.

### Key Concepts:

1. **Subject**: The entity that holds the state. When a state change occurs, it notifies all registered observers about the change.
2. **Observer**: An entity that wishes to be notified when the state of the subject changes. Observers register themselves with the subject to receive updates.
3. **ConcreteSubject**: A specific implementation of the subject interface. It maintains the real state and notifies observers about state changes.
4. **ConcreteObserver**: A specific implementation of the observer interface that performs an update action in response to a notification.

### When to Use:

- When changes to one object (the subject) require changing other objects (observers), and the number of objects that need to be changed is dynamic or unknown in advance.
- When there's a need to reduce coupling between a core component and its dependent components.

### Advantages:

- Supports the principle of loose coupling between objects that interact.
- Allows sending data to other objects effectively without knowing their specific types.

### Disadvantages:

- Observers are notified in random order, and there's no guarantee on the execution order.
- If not properly handled, it can lead to memory leaks due to lingering references in the subject's list of observers.

### Observer Pattern in Java:

Java has built-in support for the Observer Pattern in the java.util package (though it's considered somewhat deprecated in favor of more modern approaches like PropertyChangeListener in Swing). However, implementing it from scratch can provide a deeper understanding.

```java
import java.util.ArrayList;
import java.util.List;

// Subject
interface Subject {
    void registerObserver(Observer observer);
    void removeObserver(Observer observer);
    void notifyObservers();
}

// ConcreteSubject
class WeatherData implements Subject {
    private List<Observer> observers;
    private float temperature;
    
    public WeatherData() {
        observers = new ArrayList<>();
    }
    
    @Override
    public void registerObserver(Observer observer) {
        observers.add(observer);
    }
    
    @Override
    public void removeObserver(Observer observer) {
        observers.remove(observer);
    }
    
    @Override
    public void notifyObservers() {
        for (Observer observer : observers) {
            observer.update(temperature);
        }
    }
    
    public void setTemperature(float temperature) {
        this.temperature = temperature;
        notifyObservers();
    }
}

// Observer
interface Observer {
    void update(float temperature);
}

// ConcreteObserver
class CurrentConditionsDisplay implements Observer {
    private float temperature;
    
    @Override
    public void update(float temperature) {
        this.temperature = temperature;
        display();
    }
    
    public void display() {
        System.out.println("Current conditions: " + temperature + "F degrees");
    }
}

// Main class to demonstrate
public class ObserverDemo {
    public static void main(String[] args) {
        WeatherData weatherData = new WeatherData();
        CurrentConditionsDisplay currentDisplay = new CurrentConditionsDisplay();
        
        weatherData.registerObserver(currentDisplay);
        
        // Simulate new weather measurements
        weatherData.setTemperature(78.5f);
    }
}
```

In this example, `WeatherData` acts as the `ConcreteSubject`, maintaining a state (`temperature`) and notifying `Observers` about changes. `CurrentConditionsDisplay` is a `ConcreteObserver`, updating itself based on the state of `WeatherData`. When `WeatherData`'s `setTemperature` method is called, it triggers an update to all registered observers by calling `notifyObservers`.

This pattern is especially useful for maintaining consistency between related objects without making classes tightly coupled. It promotes a clean separation between the core functionality and the user interface or other dependent functionalities.