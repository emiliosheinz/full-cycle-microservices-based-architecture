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
