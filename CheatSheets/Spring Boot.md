# Spring Boot Cheatsheet

## Getting Started

### Create a Spring Boot Project
Use Spring Initializr or Spring Boot CLI to generate a new project with required dependencies.

### Run the Application
Use `java -jar` to run the compiled Spring Boot application JAR.

### Application Properties
Configure settings in `application.properties` or `application.yml` for database connections, logging, etc.

## Annotations

### `@SpringBootApplication`
Main class annotation, combines `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan`.

### `@RestController`
Indicates that a class is a RESTful controller.

### `@RequestMapping`
Maps HTTP requests to controller methods.

### `@Autowired`
Injects dependencies (beans) automatically.

### `@Service`
Indicates a service class.

### `@Repository`
Indicates a data repository class.

## Web Development

### RESTful APIs
Use `@RestController` and `@RequestMapping` for creating RESTful endpoints.

### Request Mapping
```java
@RequestMapping("/api")
public class MyController {
    //...
}
```

### Request Parameters
```java
@GetMapping("/user")
public User getUser(@RequestParam String username) {
    //...
}
```

### Path Variables
```java
@GetMapping("/user/{id}")
public User getUserById(@PathVariable Long id) {
    //...
}
```

## Data Access

### JPA Repositories
Create JPA repositories with built-in CRUD operations.

### `@Entity`
Mark a class as a JPA entity.

### `@Repository`
Indicate a JPA repository.

### Query Methods
Define methods in repositories using method names to auto-generate queries.

## Best Practices

### Use Dependency Injection
Leverage Spring's dependency injection to manage components and improve testability.

### Follow RESTful Principles
Adhere to RESTful design principles for creating clean and predictable APIs.

### Keep Business Logic in Services
Place business logic in service classes, keeping controllers lightweight.

### Use Application Properties
Store configuration settings in external properties files or environment variables.

### Implement Logging
Utilize a logging framework like Logback or Log4j for debugging and monitoring.

### Use Validation
Validate input using Spring's validation annotations or custom validation logic.

### Error Handling
Implement custom exception classes and exception handlers for proper error responses.

### Security
Secure your application using Spring Security for authentication and authorization.

### Profile Configuration
Use profiles to manage different configurations for different environments (dev, prod, etc.).

### Testing
Write unit and integration tests using JUnit and Spring Test for robust and maintainable code.

### Monitor and Actuator
Use Spring Boot Actuator to monitor application health, metrics, and manage endpoints.

Remember, these are general guidelines and practices. Always refer to the official Spring Boot documentation and community resources for the most up-to-date information and best practices.