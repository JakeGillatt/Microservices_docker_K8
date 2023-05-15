# What is Microservices?

Microservices refers to an architectural approach in software development where an application is broken down into smaller, independent, and loosely coupled services. Each service focuses on performing a specific function or business capability within the application.

Microservices are essentially building blocks that work together to create a larger application. Instead of building one monolithic application, where all functionalities are tightly integrated, microservices divide the application into smaller, self-contained units. Each microservice can be developed, deployed, and scaled independently, which provides flexibility and agility in the development process.

These microservices communicate with each other through well-defined APIs (Application Programming Interfaces). They can be developed using different programming languages, frameworks, and technologies, as long as they adhere to the agreed-upon communication protocols.

#
# Whats the difference between 2 tier architecture and microservices?

The main difference between 2-tier architecture and microservices lies in their approach to structuring and scaling applications.

2-Tier Architecture:

- In 2-tier architecture, the application is divided into two main layers: the presentation layer (client-side) and the data layer (server-side).
- The presentation layer handles the user interface and user interactions, while the data layer manages data storage and business logic.
- Communication between the client and server happens directly, often through direct method calls or queries to a database.
- Scaling is typically done vertically, by adding more resources (such as CPU or memory) to the existing servers.
- The application components are tightly coupled, meaning changes in one component can affect the others, requiring coordination and potential downtime during updates.

Microservices:

- Microservices, on the other hand, break down the application into smaller, independent services that can be developed, deployed, and scaled independently.
- Each microservice is responsible for a specific function or business capability, and they communicate with each other through well-defined APIs.
- Microservices can be developed using different technologies, languages, and frameworks, as long as they adhere to the agreed-upon communication protocols.
- Scaling can be done horizontally, by adding more instances of specific microservices as needed, which allows for more granular scalability.
- The loosely coupled nature of microservices allows for independent development and deployment, making it easier to update or replace individual services without affecting the entire application.

2-tier architecture has two main layers with direct communication, while microservices consist of smaller, independent services that communicate via APIs. 

#
# What is Docker?

Docker is an open-source platform that allows developers to automate the deployment, packaging, and running of applications within isolated containers. Containers are lightweight, standalone environments that encapsulate all the necessary dependencies and libraries required to run an application.

Think of Docker as a tool that creates virtual containers for applications. These containers package the application code along with its dependencies, configuration files, and libraries into a single, self-contained unit. This ensures that the application can run consistently across different environments, such as development, testing, and production, without any compatibility issues.

#
# What is Containerisation?

Containerization is a technique used in software development and deployment that allows applications to run in isolated and portable environments called containers. Containers encapsulate an application along with its dependencies, libraries, and configuration files, providing a consistent and reliable runtime environment.

Docker enables the containerization of applications, which means each application and its dependencies are isolated within its own container. This isolation ensures that the application can run consistently and reliably across different systems.

#
# Virtualisation vs Containerisation?

Virtualization abstracts the hardware resources to create complete virtual machines, while Containerization abstracts the operating system resources to create lightweight and isolated containers. Virtualization provides stronger isolation but with higher resource usage, while containerization offers lighter isolation with lower resource overhead. Both approaches have their advantages and are used based on specific requirements and use cases.
