# Spring Kafka Cheatsheet

## Getting Started

### Add Spring Kafka Dependency
Include the Spring Kafka dependency in your project's build configuration.

### Kafka Configuration
Configure Kafka properties in your application configuration.

### Kafka Template
Use `KafkaTemplate` to send messages to Kafka topics.

## Producer

### KafkaTemplate
```java
@Autowired
private KafkaTemplate<String, String> kafkaTemplate;

public void sendMessage(String topic, String message) {
    kafkaTemplate.send(topic, message);
}
```

### Producer Acknowledgment
```java
kafkaTemplate.send(topic, message)
    .addCallback(success -> {
        // success logic
    }, failure -> {
        // failure logic
    });
```

## Consumer

### Kafka Listener
```java
@KafkaListener(topics = "my-topic")
public void listen(String message) {
    // consume message
}
```

### Group ID
```java
@KafkaListener(topics = "my-topic", groupId = "my-group")
public void listen(String message) {
    // consume message
}
```

## Consumer with POJOs

### Consumer for POJOs
```java
@KafkaListener(topics = "my-topic", groupId = "my-group")
public void listen(User user) {
    // consume User object
}
```

### Deserialization
Configure the deserializer for POJOs in your application configuration.

## Error Handling

### Error Handling in Listener
```java
@KafkaListener(topics = "my-topic")
public void listen(String message, @Header(KafkaHeaders.RECEIVED_TOPIC) String topic) {
    try {
        // consume message
    } catch (Exception e) {
        // handle error
    }
}
```

## Best Practices

- Use meaningful topic names to represent the data being exchanged.
- Configure proper serializer and deserializer for message data.
- Group consumers with the same `groupId` to achieve load balancing and fault tolerance.
- Handle exceptions and errors gracefully in Kafka listeners.
- Ensure proper error handling to prevent message processing failures.
- Leverage Kafka headers to extract metadata from messages.
- Test your Kafka integration with various scenarios, including retries and errors.
- Monitor Kafka using tools like Kafka Manager or Confluent Control Center.

Remember, Spring Kafka simplifies working with Kafka in a Spring application, but understanding Kafka concepts like topics, partitions, and consumer groups is crucial for effective usage. Always refer to the official Spring Kafka documentation and community resources for detailed information.