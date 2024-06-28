# Microservices-based Architecture

According to Google[^1], **Microservices** architecture is a design approach in software development where a large application is composed of small, loosely coupled, and independently deployable services. Each service is usually responsible for a specific business functionality and communicates with other services through well-defined APIs. This architecture enables organizations to develop, deploy, and scale parts of the application independently, facilitating continuous delivery and deployment, enhancing fault isolation, and enabling the use of diverse technologies and platforms suited to each service's requirements.

[^1]: https://cloud.google.com/learn/what-is-microservices-architecture

## Microservices VS Monolithic Architecture

In a **Monolithic** architecture, the entire application is developed as a single unit, and all its components are usually tightly coupled. This architecture is simple to develop and test but becomes complex and challenging to maintain as the application grows. In contrast, a **Microservices** architecture breaks down the application into small, manageable services that are loosely coupled. This architecture is more complex to develop and test but, on the other hand, is easier to maintain and scale as the application grows.

**Microservices:**

- Focused on a single business functionality
- Allow the use of diverse technologies and platforms
- Independently deployable

**Monolithic:**

- Developed as a single unit that solves all business functionalities
- Usually developed using a single technology stack
- Deployed as a single unit

## When should I use Microservices?

- **To scale teams:** Microservices architecture enables teams to work independently on various services, allowing them to scale efficiently as the project expands.

- **With well-defined business functionalities:** Since microservices architecture is complex to develop and test, it's best suited for projects where the business functionalities are already clearly defined.

- **With mature deployment processes:** Microservices architecture relies on continuous delivery and deployment, making it ideal for organizations with established and mature deployment processes.

- **For independent scaling of application components:** Microservices architecture allows different parts of the application to be scaled independently, which is beneficial when such flexibility is required.

- **When specific technologies are needed for different services:** Different problems may be better solved using specific technologies. Microservices architecture allows you to use the best technology for each service, making it ideal for projects where diverse technologies are required.

## When should I use Monolithic Architecture?

- **To start a brand new project:** Monolithic architecture is simpler to develop and test, making it a good choice for starting projects.

- **When you don't have a clear understanding of the business functionalities:** Since Monolithic Services are not focused on a single business functionality, they are more flexible and can be used when the business functionalities are not clearly defined.

- **You wan't to have more control over the used technologies:** Monolithic architecture is usually developed using a single technology stack, making it ideal for projects where you want to have more control over the technologies used.

- **For easier hiring and onboarding:** Since monolithic services are usually developed using a single technology stack, and have their components tightly coupled, in a single place they are easier to understand, making it easier to hire and onboard new developers.

- **When you want easier sharing of code and data:** Monolithic architecture has all its components in a single place, making it easier to share code and data between different components of the application.

## Migration from Monolithic to Microservices Architectures

Migrating from a Monolithic to a Microservices architecture is a complex process that requires careful planning and execution. Here are some key steps to consider when migrating:

1. **Identify business functionalities:** Identify the different business functionalities of the application and break them down into separate services. Better understanding DDD (Domain-Driven Design) can help in this process.

1. **Avoid too much granularity:** Avoid breaking down the application into too many microservices, as this can lead to complexity and performance issues.

1. **Check for dependencies:** Identify dependencies between different components of the application and ensure that they are properly managed in the microservices architecture. This can avoid you from having a distributed monolith.

1. **Plan the migration of the database:** Migrating from a monolithic database to a microservices architecture can be challenging. Plan the migration carefully and consider using separate databases for each service.

1. **Don't be afraid about data duplication:** In a microservices architecture, it's common to have data duplication between services. This can help improve performance and scalability.

1. **Eventual consistency:** In a microservices architecture, services communicate asynchronously through events. This can lead to eventual consistency issues that need to be carefully managed.

1. **Start from the edges:** Start by breaking down the application from the edges, i.e., the parts of the application that are more loosely coupled. This can help you gain experience with microservices architecture before tackling the more complex parts of the application.

## Characteristics of a Microservice Architecture

The _Characteristics of a Microservice Architecture_ section in Martin Fowler's article[^2] on microservices highlights several key features of this architectural style:

[^2]: https://martinfowler.com/articles/microservices.html

1. **Componentization via Services:** Microservices break down an application into smaller, independent services. Each service is a component that can be developed, deployed, and scaled independently.

1. **Organized Around Business Capabilities:** Unlike traditional monolithic architectures which are often organized around technical layers (e.g., UI, business logic, database), microservices should be structured around business capabilities. Each service focuses on a specific business function.

1. **Products, Not Projects:** Teams using microservices are aligned to long-lived products rather than short-term projects. This encourages a focus on continuous delivery and improvement.

1. **Smart Endpoints and Dumb Pipes:** Microservices emphasize smart endpoints that handle the logic and processing, while the communication pipes between services are simple. This contrasts with traditional enterprise service buses that handle much of the processing.

1. **Decentralized Governance:** Microservice architectures favor decentralized governance and diverse technology stacks. This allows teams to choose the best tools and technologies for their specific needs.

1. **Decentralized Data Management:** Each microservice manages its own database, which helps avoid the complexities of a single centralized database and allows for polyglot persistence (using different data storage technologies).

1. **Infrastructure Automation:** The adoption of DevOps practices, continuous integration, and continuous deployment are essential. Automation of infrastructure and deployment processes is critical to manage the complexity of multiple services.

1. **Design for Failure:** Microservices are designed to handle failure gracefully. Each service should be resilient and able to recover from failures, minimizing the impact on the overall system.

1. **Evolutionary Design:** The architecture supports the evolutionary design, allowing systems to evolve over time. This is crucial for adapting to changing business requirements and technologies.

## Resilience in Microservices Architecture

Resilience is the ability of a system to recover from failures and continue to function. It reduces the risks of data loss, downtime, and service disruptions. In a microservices architecture, resilience is crucial due to the distributed nature of the services. Here are some key strategies to improve resilience in microservices:

1. **Protect and be protected:** A service in a distributed architecture should adopt mechanisms to preserve its own integrity and protect itself from failures. At the same time, it should be designed to be resilient to failures in other services.

1. **Health Checks:** Implement health checks to monitor the system's status and detect failures early, allowing you to take corrective actions before they impact users. It's important to mention that health checks should actually check the system's health, not just return a HTML with 200 status code.

1. **Rate Limiting:** Implement rate limiting to prevent abuse and protect the system from excessive traffic, ensuring that it remains responsive and available to legitimate users.

1. **Circuit Breaker:** Circuit breakers can be used to temporarily block requests to a failing service and redirect them to a fallback mechanism. Preventing cascading failures.

1. **API Gateway:** An API Gateway can be used to manage incoming requests, enforce policies, and provide a unified interface to the underlying services. It's important to mention that it can be use to implement rate limiting and circuit breakers, for example.

1. **Service Mesh:** A service mesh can be used to manage service-to-service communication, provide observability, and enforce security policies. It can also help with resilience by providing features like circuit breaking, retries, and timeouts.
