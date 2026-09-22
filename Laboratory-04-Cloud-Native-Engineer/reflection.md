# Mission Reflection

Laboratory Activity 4 helped me understand how containerization is changing the way applications are deployed in cloud environments. One of the main differences I learned is that Docker containers can start much faster than Virtual Machines. A VM needs to boot a complete operating system before an application can run, while a container shares the host operating system kernel and only needs the required application and dependencies. Because of this, containers are generally lightweight and faster to deploy.

Port mapping using `-p 8080:80` is necessary because it connects a port on the host machine to a port inside the container. In this activity, Nginx listens on port 80 inside the container, while port 8080 on the host allows me to access the web server through `http://localhost:8080`. Without the correct port mapping, I would not be able to access the service through that host port.

When the `docker rm` command is used, the specified stopped container is permanently removed. Any data stored only inside the writable layer of that container is deleted along with it. However, Docker images and separately stored volumes are not automatically removed by this command.

Containerization also changes how software developers and IT operations teams work together. Developers can package applications with their dependencies, while operations teams can deploy the same containers across different environments. This improves consistency and supports DevOps practices by encouraging collaboration, automation, and faster application delivery.

My GitHub portfolio is evolving as I add more laboratory activities and practical experiences. In this laboratory, I expanded my knowledge from basic cloud infrastructure and multi-cloud concepts to container deployment and management. By documenting commands, screenshots, and reflections, my portfolio is becoming a record of both my technical skills and my learning progress in cloud computing.
