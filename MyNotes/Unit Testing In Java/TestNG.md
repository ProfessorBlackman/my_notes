## Definition:
- for writing unit tests.
- similar to JUnit.

## Benefits:
- More powerful and flexible than JUnit.
- Easier to write and maintain unit tests.
- Provides features for data-driven testing and parallel testing.

1. **Setup TestNG**:
   - If you're using Maven, you can include TestNG in your project by adding the following dependency to your `pom.xml`:

     ```xml
     <dependency>
         <groupId>org.testng</groupId>
         <artifactId>testng</artifactId>
         <version>x.x.x</version> <!-- Replace x.x.x with the latest version -->
         <scope>test</scope>
     </dependency>
     ```

   - For Gradle, add the following dependency to your `build.gradle`:

     ```groovy
     testImplementation 'org.testng:testng:x.x.x' // Replace x.x.x with the latest version
     ```

2. **Create Test Classes**:
   - TestNG tests are written in Java classes. You can create a test class by annotating it with `@Test` and writing test methods:

     ```java
     import org.testng.annotations.Test;

     public class MyTest {

         @Test
         public void testMethod() {
             // Test code goes here
         }
     }
     ```

3. **TestNG Annotations**:
   - TestNG provides a set of annotations to control the flow of test execution. Some commonly used annotations include:
     - `@Test`: Marks a method as a test method.
     - `@BeforeSuite`, `@AfterSuite`: Methods annotated with these will run before/after all tests in a suite.
     - `@BeforeTest`, `@AfterTest`: Methods annotated with these will run before/after all tests within a `<test>` tag in the testng.xml file.
     - `@BeforeClass`, `@AfterClass`: Methods annotated with these will run before/after all test methods in a class.
     - `@BeforeMethod`, `@AfterMethod`: Methods annotated with these will run before/after each test method.

4. **TestNG XML Configuration**:
   - TestNG allows you to configure your tests using an XML file. You can specify test classes, suites, parameters, and more in this file. Here's a basic example:

     ```xml
     <!DOCTYPE suite SYSTEM "http://testng.org/testng-1.0.dtd">
     <suite name="MySuite">
       <test name="MyTest">
         <classes>
           <class name="com.example.MyTest"/>
         </classes>
       </test>
     </suite>
     ```

5. **Running Tests**:
   - You can run TestNG tests using various methods:
     - Run tests directly from your IDE (e.g., IntelliJ IDEA, Eclipse).
     - Use the TestNG command-line tool.
     - Integrate TestNG with build tools like Maven or Gradle.

6. **TestNG Assertions**:
   - TestNG provides a set of built-in assertions for verifying expected outcomes. Some commonly used assertions include:
     - `assertEquals(expected, actual)`: Verifies that two values are equal.
     - `assertTrue(condition)`, `assertFalse(condition)`: Verifies that a condition is true/false.
     - `assertNotNull(object)`, `assertNull(object)`: Verifies that an object is not null/null, respectively.
     - `assertThrows(exceptionType, executable)`: Verifies that an exception of the specified type is thrown by the executable code.

7. **Test Groups**:
   - TestNG allows you to categorize your tests into groups and execute specific groups of tests. You can use the `@Test` annotation's `groups` attribute to assign tests to groups and specify which groups to run in the testng.xml file.

## Comparation With JUnit:
TestNG and JUnit are both popular testing frameworks for Java, and they share many similarities in their basic functionalities. However, they also have some differences in features and philosophies. Here's a comparison between TestNG and JUnit:

1. **Annotations**:
   - Both frameworks support annotations to define test methods, setup, and tear down methods. TestNG provides a more extensive set of annotations for test configuration, such as defining test groups, specifying test dependencies, and configuring parallel execution.

2. **Parameterized Tests**:
   - JUnit provides built-in support for parameterized tests using the `@ParameterizedTest` annotation (in JUnit 5). TestNG also supports parameterized tests through its `@DataProvider` annotation, allowing you to define data sources for test methods.

3. **Assertions**:
   - Both frameworks provide built-in assertion methods for verifying expected outcomes. The assertion methods in JUnit are part of the `org.junit.Assert` class, while TestNG has its own set of assertion methods. TestNG's assertions are more similar to those in JUnit 5, providing a richer set of options and clearer failure messages.

4. **Test Dependency**:
   - TestNG allows you to specify dependencies between test methods using the `dependsOnMethods` attribute in the `@Test` annotation. This feature enables you to ensure that certain tests are executed only after specific setup steps or prerequisite tests pass. JUnit doesn't have built-in support for test dependencies.

5. **Test Groups**:
   - TestNG supports the concept of test groups, allowing you to categorize tests and execute specific groups of tests selectively. You can use the `groups` attribute in the `@Test` annotation to assign tests to groups and configure which groups to run in the testng.xml file. JUnit doesn't have built-in support for test groups.

6. **Parallel Execution**:
   - TestNG provides native support for parallel execution of tests, enabling you to run tests concurrently across multiple threads or processes. This can significantly reduce test execution time, especially for large test suites. JUnit doesn't have built-in support for parallel execution, although you can achieve parallelism using external tools or frameworks.

7. **Test Configuration**:
   - TestNG allows you to configure tests using an XML file (testng.xml), where you can specify test classes, suites, parameters, listeners, and more. This provides greater flexibility in test configuration and execution. JUnit typically relies on annotations and programmatic configuration for test setup.

8. **Listeners and Reporters**:
   - Both frameworks support listeners and reporters for extending test behavior and generating test reports. However, TestNG provides a more extensive set of listeners and reporters out-of-the-box, allowing you to customize test execution and reporting more easily.