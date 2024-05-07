## Introduction to JavaFX

JavaFX is a Java library used for building cross-platform desktop applications with rich graphical user interfaces (GUIs).

## Getting Started

1. **Setup:**
   - Ensure JDK is installed.
   - Setup IDE (Eclipse, IntelliJ IDEA, NetBeans) or use command-line tools.
   - Import JavaFX libraries.

2. **Project Structure:**
   - Main Class: Contains the main method to launch the application.
   - FXML files: XML-based markup language for designing UI layouts.
   - Controller Classes: Java classes to control UI behavior.

## Basics

### Hello World Example

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.stage.Stage;

public class HelloWorld extends Application {

    @Override
    public void start(Stage primaryStage) {
        Label label = new Label("Hello, World!");
        Scene scene = new Scene(label, 200, 100);
        primaryStage.setScene(scene);
        primaryStage.setTitle("Hello World Application");
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

### UI Controls

- **Button:** `Button`
- **Label:** `Label`
- **Text Field:** `TextField`
- **Password Field:** `PasswordField`
- **Combo Box:** `ComboBox`
- **Check Box:** `CheckBox`
- **Radio Button:** `RadioButton`
- **Toggle Button:** `ToggleButton`
- **Slider:** `Slider`
- **Progress Bar:** `ProgressBar`
- **Menu:** `Menu`, `MenuItem`

### Layouts

- **VBox:** Vertical box layout.
- **HBox:** Horizontal box layout.
- **BorderPane:** Divides the space into five regions: top, right, bottom, left, and center.
- **GridPane:** Grid-based layout.

### Event Handling

- **Action Event:** Handle user actions (e.g., button clicks).
- **Key Event:** Handle keyboard events.
- **Mouse Event:** Handle mouse clicks and movements.

## Advanced Features

1. **CSS Styling:** Style UI components using CSS.
2. **FXML:** Separate UI design from application logic using FXML.
3. **Charts:** Display data using bar, line, pie, etc., charts.
4. **Canvas:** Draw shapes, images, and text directly onto a canvas.
5. **Media:** Play audio and video files.
6. **Concurrency:** Execute tasks concurrently using `Platform.runLater()`.

## Debugging and Tools

1. **Scene Builder:** Drag-and-drop UI design tool for FXML.
2. **Debugging:** Use IDE debuggers for step-by-step debugging.
3. **Logging:** Utilize logging frameworks like Log4j for logging.

## Best Practices

1. **Separation of Concerns:** Separate UI design, logic, and data.
2. **UI Responsiveness:** Update UI components on the JavaFX Application Thread.
3. **Memory Management:** Avoid memory leaks by properly managing UI component references.

## Resources

- Official Documentation: [JavaFX Documentation](https://openjfx.io/javadoc/)
- Tutorials: [JavaFX Tutorial](https://openjfx.io/openjfx-docs/)
- Community Support: [JavaFX Community](https://stackoverflow.com/questions/tagged/javafx)

This cheat sheet covers the basics, advanced features, debugging tools, best practices, and additional resources for JavaFX development. Explore the official documentation and community resources for more detailed information on specific topics.