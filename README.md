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
# Microservices diagram:

![microservices](https://github.com/JakeGillatt/Microservices_docker_K8/assets/129315605/b8abf05b-d83a-4af3-b76a-c1d2653396d0)

#
# What is Docker?

Docker is an open-source platform that allows developers to automate the deployment, packaging, and running of applications within isolated containers. Containers are lightweight, standalone environments that encapsulate all the necessary dependencies and libraries required to run an application.

Think of Docker as a tool that creates virtual containers for applications. These containers package the application code along with its dependencies, configuration files, and libraries into a single, self-contained unit. This ensures that the application can run consistently across different environments, such as development, testing, and production, without any compatibility issues.

#
# Docker Architecture diagram:

![Docker diagram](https://github.com/JakeGillatt/Microservices_docker_K8/assets/129315605/4a665f4d-809e-4c3c-b93c-2a538b4270ad)

#
# What is Containerisation?

Containerization is a technique used in software development and deployment that allows applications to run in isolated and portable environments called containers. Containers encapsulate an application along with its dependencies, libraries, and configuration files, providing a consistent and reliable runtime environment.

Docker enables the containerization of applications, which means each application and its dependencies are isolated within its own container. This isolation ensures that the application can run consistently and reliably across different systems.

#
# Virtualisation vs Containerisation?

Virtualization abstracts the hardware resources to create complete virtual machines, while Containerization abstracts the operating system resources to create lightweight and isolated containers. Virtualization provides stronger isolation but with higher resource usage, while containerization offers lighter isolation with lower resource overhead. Both approaches have their advantages and are used based on specific requirements and use cases.


#
# Launching a Docker container and setting up Nginx

- We can run `docker run hello-world` to test that docker will download an image and run it
1. In a git bash terminal, run the command `docker run -d -p 80:80 nginx` to install and run nginx on port 80
- We can use `docker ps` to display the containers that are running
- We can use `docker stop <container id>` to stop a container
- We can use `docker start <container id>` to start up a container
- We can use `docker rm <container id> -f` to delete a container entirely
- These three commands are called the docker container lifecycle
2. In your local browser enter `localhost` to check nginx is available
3. Run `apt-get update -y` and `apt upgrade -y` to update the container
4. Install sudo with `apt install sudo`
5. Install nano with `sudo apt install nano -y`
6. Run `docker exec -it <container id> /bin/bash` and then `alias docker="winpty docker"`
7. Enter `docker exec -it <container id> sh` to go into the container
- As an example we edited the nginx index.html file:
8. Using  `cd /usr/share/nginx/html` we then `sudo nano index.html` to edit the file and we entered our own text
9. Save the file and check the changes in the local browser

#
# Pushing a Container Image and any changes, to your Docker Hub repo

1. Run the command `docker commit <container_id> <your_new_image_name>`
2. Run `docker tag <your_new_image_name> <dockerhub_username>/<repository_name>:<newtag>`
3. Run `docker login` and log in to your docker hub
4. Run `docker push <dockerhub_username>/<repository_name>:<tag>`

- To save and push any changes after completing this, run `docker commit <container id>` and then `docker push <dockerhub_username>/<repository_name>:<tagname>`
- Your changes will now be pushed to your Docker Hub repo

- To download and run an image on port 90, use `docker run -d -p 90:80 <username>/<repo>:<tagname>`
