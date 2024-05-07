## Mockito:
### Definition:
- used to create mock objects that simulate the behavior of real objects. This is useful for isolating code to be tested from it's dependencies.
## Benefits:
- Improves test isolation and maintainability
- Makes tests more readable and easier to understand
- Allows you to test code that depends on external systems or services

## How to use:
1. **Setup Mockito**: You need to include the Mockito library in your project. You can do this either by downloading the JAR file from the Mockito website or by using a dependency management tool like Maven or Gradle.

    For Maven, add the following dependency to your `pom.xml` file:

    ```xml
    <dependency>
        <groupId>org.mockito</groupId>
        <artifactId>mockito-core</artifactId>
        <version>x.x.x</version> <!-- Replace x.x.x with the latest version -->
        <scope>test</scope>
    </dependency>
    ```

    For Gradle, add the following dependency to your `build.gradle` file:

    ```groovy
    testImplementation 'org.mockito:mockito-core:x.x.x' // Replace x.x.x with the latest version
    ```

2. **Create a Test Class**: Start by creating a test class for the class you want to test. Let's say you have a class `Calculator`:

    ```java
    public class Calculator {
        public int add(int a, int b) {
            return a + b;
        }
    }
    ```

    You can create a test class for `Calculator` using JUnit:

    ```java
    import org.junit.Test;
    import static org.junit.Assert.assertEquals;

    public class CalculatorTest {

        @Test
        public void testAdd() {
            Calculator calculator = new Calculator();
            assertEquals(5, calculator.add(2, 3));
        }
    }
    ```

3. **Mock Dependencies**: If your class has dependencies, you can mock them using Mockito. For example, if `Calculator` depends on a `Logger` class:

    ```java
    import org.junit.Test;
    import static org.junit.Assert.assertEquals;
    import static org.mockito.Mockito.mock;
    import static org.mockito.Mockito.when;

    public class CalculatorTest {

        @Test
        public void testAdd() {
            Logger loggerMock = mock(Logger.class);
            Calculator calculator = new Calculator(loggerMock);
            when(loggerMock.log("Adding 2 and 3")).thenReturn("Logged successfully");
            assertEquals(5, calculator.add(2, 3));
        }
    }
    ```

    In this example, `Logger` is mocked using `mock(Logger.class)`, and its behavior is stubbed using `when(loggerMock.log("Adding 2 and 3")).thenReturn("Logged successfully")`.

4. **Verify Interactions**: You can also use Mockito to verify that certain interactions with mock objects occur during the test. For example:

    ```java
    import org.junit.Test;
    import static org.mockito.Mockito.mock;
    import static org.mockito.Mockito.verify;

    public class CalculatorTest {

        @Test
        public void testAdd() {
            Logger loggerMock = mock(Logger.class);
            Calculator calculator = new Calculator(loggerMock);
            calculator.add(2, 3);
            verify(loggerMock).log("Adding 2 and 3");
        }
    }
    ```

    Here, `verify(loggerMock).log("Adding 2 and 3")` verifies that the `log` method of the `Logger` mock was called with the specified arguments.


# Other Features

1. **Mocking Objects**:
   - `mock(Class<T> classToMock)`: Creates a mock object of the specified class.
   - `@Mock`: Annotation to create a mock object, used with MockitoJUnitRunner or MockitoAnnotations.initMocks().

2. **Stubbing Behavior**:
   - `when(mock.methodCall()).thenReturn(value)`: Stubs the behavior of a method call on a mock object.
   - `doReturn(value).when(mock).methodCall()`: Alternative way to stub the behavior of void methods.
   - `doThrow(exception).when(mock).methodCall()`: Stubs the behavior to throw an exception when a method is called.

3. **Verifying Interactions**:
   - `verify(mock).methodCall()`: Verifies that a method was called on a mock object.
   - `verify(mock, times(n)).methodCall()`: Verifies that a method was called a specific number of times.
   - `verify(mock, never()).methodCall()`: Verifies that a method was never called.
   - `verifyNoMoreInteractions(mock)`: Verifies that no other methods were called on the mock object.

4. **Argument Matchers**:
   - `any(Class<T> type)`: Matches any object of the specified type.
   - `eq(value)`: Matches the specified value.
   - `anyInt()`, `anyString()`, etc.: Matches any value of the specified type.

5. **Capturing Arguments**:
   - `ArgumentCaptor<T> captor = ArgumentCaptor.forClass(T.class)`: Captures arguments passed to a method.
   - `captor.getValue()`: Retrieves the captured argument.

6. **Resetting Mocks**:
   - `reset(mock)`: Resets the mock object, clearing any recorded interactions and stubbed behavior.

7. **Annotations**:
   - `@Mock`: Creates a mock object.
   - `@InjectMocks`: Injects mocks into the tested object automatically.
   - `@Captor`: Declares an argument captor.

8. **Spying**:
   - `spy(Object obj)`: Creates a spy object that delegates to the real object.
   - `when(spy.methodCall()).thenReturn(value)`: Stubs behavior on a spy object.

9. **MockitoJUnitRunner**:
   - `@RunWith(MockitoJUnitRunner.class)`: Runs tests with Mockito support.

10. **MockitoAnnotations**:
    - `MockitoAnnotations.initMocks(Object testClass)`: Initializes annotated fields in the specified test class.