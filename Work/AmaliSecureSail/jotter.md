Certainly! To use **UUIDs** as identifiers in MongoDB with Spring Boot, follow these steps:

1. **Configure UUID Support**:
    
    - In your Spring Boot application, configure the MongoDB driver to handle UUIDs. Specify the `uuidRepresentation` parameter in your MongoDB client setup.
    - If you’re using Java configuration, create a `MongoClient` bean and set the `uuidRepresentation` to `UuidRepresentation.STANDARD`:
        
        ```java
        @Bean
        public MongoClient mongo() throws Exception {
            ConnectionString connectionString = new ConnectionString("mongodb://localhost:27017/test");
            MongoClientSettings mongoClientSettings = MongoClientSettings.builder()
                    .uuidRepresentation(UuidRepresentation.STANDARD)
                    .applyConnectionString(connectionString)
                    .build();
            return MongoClients.create(mongoClientSettings);
        }
        ```
        
    - Alternatively, if you’re using `application.properties`, add the following line:
        
        ```
        spring.data.mongodb.uuid-representation=standard
        ```
        
2. **Define an Abstract Base Class**:
    
    - Create an abstract class (e.g., `UuidIdentifiedEntity`) that defines the UUID identifier for all your MongoDB document classes:
        
        ```java
        public abstract class UuidIdentifiedEntity {
            @Id
            protected UUID id;
        
            public void setId(UUID id) {
                if (this.id != null) {
                    throw new UnsupportedOperationException("ID is already defined");
                }
                this.id = id;
            }
        
            // Getter
        }
        ```
        
    - Assume that all classes persisted in the MongoDB database inherit from this base class.
3. **Generate UUIDs**:
    
    - Use Spring’s lifecycle events to generate UUIDs before converting Java objects to MongoDB documents.
    - Extend `AbstractMongoEventListener` and override the `onBeforeConvert` method:
        
        ```java
        public class UuidIdentifiedEntityEventListener extends AbstractMongoEventListener<UuidIdentifiedEntity> {
            @Override
            public void onBeforeConvert(BeforeConvertEvent<UuidIdentifiedEntity> event) {
                super.onBeforeConvert(event);
                UuidIdentifiedEntity entity = event.getSource();
                if (entity.getId() == null) {
                    entity.setId(UUID.randomUUID());
                }
            }
        }
        ```
        
    - This event listener ensures that UUIDs are set before saving documents.

Now you can use UUIDs as identifiers for your MongoDB documents in Spring Boot! 🌟

[For more details, you can refer to the](https://www.baeldung.com/java-mongodb-uuid) [1](https://www.baeldung.com/java-mongodb-uuid).