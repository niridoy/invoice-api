# invoice-api

src/main/java/com/company/invoice-api
├── domain
│   ├── model            // Core domain models (entities, value objects)
│   ├── repository       // Domain-driven repositories (interfaces)
│   ├── service          // Domain services
│   ├── event            // Domain events
│   └── factory          // Factories for creating complex domain objects
├── application
│   ├── dto              // Data Transfer Objects
│   ├── service          // Application services (use cases)
│   ├── mapper           // Mappers between DTOs and domain models
│   ├── event            // Application event handlers
│   └── exception        // Application-specific exceptions
├── infrastructure
│   ├── config           // Configuration (Spring, security, etc.)
│   ├── persistence      // JPA/Hibernate-based repository implementations
│   ├── messaging        // Messaging components (Kafka, RabbitMQ, etc.)
│   ├── external         // Integrations with external systems
│   └── util             // Utility classes
├── web
│   ├── controller       // REST controllers
│   ├── request          // Request objects
│   └── response         // Response objects
└── tests                // Unit and integration tests
