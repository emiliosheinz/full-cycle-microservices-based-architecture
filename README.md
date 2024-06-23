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
