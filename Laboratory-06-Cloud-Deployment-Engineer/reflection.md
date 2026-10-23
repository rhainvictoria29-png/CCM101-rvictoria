# Mission 6 Reflection — The Cloud Deployment Engineer

In this laboratory activity, I learned how Docker Compose can make cloud deployment easier and more organized. Before this activity, I understood that containers could run applications separately, but I did not fully understand how multiple containers could work together as one system. By using Nextcloud and MariaDB, I learned how a web application communicates with a database.

Writing a `docker-compose.yml` file makes an engineer's job easier because the configuration is saved in one file instead of requiring many commands to be entered manually. It also makes deployment more consistent and repeatable. With Docker Compose, I can start or stop the entire application stack using a single command.

I also learned that YAML indentation is very important. If I accidentally use a Tab instead of spaces or place a setting under the wrong section, Docker Compose may fail to read the configuration. This taught me to check the formatting carefully before deploying the containers.

Environment variables, such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_HOST`, help configure the services and establish the connection between Nextcloud and MariaDB. I learned that the database service name can be used as the database host because Docker Compose provides networking between the services. However, I also understand that demonstration passwords should not be reused in a real production environment.

Deploying Nextcloud was a valuable experience because it showed me how several components can be configured and launched together in a short time. It also helped me understand the importance of checking container status, accessing the application through a browser, and shutting down the deployment properly.

Since Mission 1, my understanding of cloud computing has developed from learning basic cloud concepts to gaining practical experience with Linux, containers, configuration files, and application deployment. I now understand better how cloud engineers use automation to manage infrastructure efficiently. This activity encouraged me to continue learning about containerization, cloud services, and infrastructure automation.

Overall, Mission 6 helped me improve my technical skills and understand why organized configuration and proper documentation are important in cloud computing.
