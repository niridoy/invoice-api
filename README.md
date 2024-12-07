# invoice-api

# For Large Scale
## 1. Domain
The core domain logic of the application.

- **`domain/model`**: Core domain models (entities and value objects).
- **`domain/repository`**: Domain-driven repository interfaces for data access.
- **`domain/service`**: Domain services encapsulating business logic.
- **`domain/event`**: Domain events to represent business happenings.
- **`domain/factory`**: Factories for creating complex domain objects or aggregates.

---

## 2. Application
Defines the use cases and application logic.

- **`application/dto`**: Data Transfer Objects for input/output operations.
- **`application/service`**: Application services orchestrating business operations.
- **`application/mapper`**: Mappers for converting between domain objects and DTOs.
- **`application/event`**: Application event handlers to process domain events.
- **`application/exception`**: Application-specific exceptions.

---

## 3. Infrastructure
Provides technical implementations and integrations.

- **`infra/config`**: Configuration for Spring, security, and other settings.
- **`infra/persistence`**: JPA/Hibernate implementations for repositories.
- **`infra/messaging`**: Messaging components like Kafka, RabbitMQ, etc.
- **`infra/external`**: Integrations with external systems or APIs.
- **`infra/util`**: Utility classes for common functionalities.

---

## 4. Web
Handles HTTP interactions and the API layer.

- **`web/controller`**: REST controllers for handling HTTP requests.
- **`web/request`**: Request objects representing API input payloads.
- **`web/response`**: Response objects representing API output payloads.

---

## 5. Tests
Contains unit and integration tests.

- **`tests`**: Organized tests to validate application functionality.
# For medium & small scale
## 1. Domain
Core domain logic of the application.

- **`domain/model`**: Core domain models (entities and value objects).
- **`domain/repository`**: Repository interfaces for data access.
- **`domain/service`**: Domain services encapsulating business logic.

## 2. Application
Defines the use cases and application logic.

- **`application/dto`**: Data Transfer Objects (DTOs) for input/output operations.
- **`application/service`**: Application services orchestrating business operations.
- **`application/exception`**: Application-specific exceptions.

## 3. Infrastructure
Technical implementations and integrations.

- **`infrastructure/config`**: Spring and security configuration.
- **`infrastructure/persistence`**: Database repositories & integrations.
- **`infrastructure/messaging`**: Messaging components (e.g., Kafka, RabbitMQ).

## 4. Web
Handles HTTP interactions and the API layer.

- **`web/controller`**: REST controllers for HTTP requests.
- **`web/dto`**: Request/Response objects for API interactions.

## 5. Tests
Unit and integration tests.

- **`tests`**: Organized tests to validate functionality.

# Tests Summary Table

| **Layer**                | **Feature Test** | **Unit Test** | **Skip/Partial** |
|--------------------------|------------------|---------------|------------------|
| **Domain**               | ✅               | ✅            |                  |
| **Application**          | ✅               | ✅            |                  |
| **Infrastructure**       | ✅ (e.g., DB, messaging) | ✅ (for utilities) | Config, unless complex |
| **Web**                  | ✅               | ✅ (controllers) |                  |
| **Simple DTOs/Utilities**|                  | ✅ (if complex) | ✅ (if trivial)  |

---

## Key Recommendations

1. **Focus testing on business logic (domain and application layers).**
2. **Write integration tests for persistence, messaging, and APIs.**
3. **Minimize or skip tests for boilerplate configuration and simple data classes.**

