# Mission Reflection

A host-based firewall protects a server by controlling incoming and outgoing network connections directly on the machine. Even if an attacker gets past the physical network perimeter, the firewall provides another layer of protection by blocking unauthorized connections. This helps prevent attackers from accessing services and applications that should not be publicly available.

Managing open network ports is important because every unnecessary open port can become a possible entry point for attackers. By allowing only the ports needed by the server, we reduce its attack surface and limit the services that outsiders can access. In this activity, I allowed SSH and TCP port 8080 because they were needed for server administration and the Nginx web application.

In a real enterprise environment, leaving MySQL port 3306 open to the public internet is dangerous because it exposes the database to unauthorized access attempts. Attackers may try to guess passwords, exploit database vulnerabilities, or access sensitive company information. Database ports should only be accessible to authorized users and systems that need them.

Completing this mission changed my perspective because I realized that having a running server does not automatically mean it is secure. Even a simple web application can become vulnerable if its network access is not properly controlled. I learned that firewall configuration, proper port management, and the Principle of Least Privilege are important practices for protecting cloud servers.

After completing eight missions, my GitHub portfolio has become more organized and meaningful. It now contains different cloud computing activities, technical documentation, commands, and screenshots that demonstrate my learning progress. This mission also helped me understand the importance of documenting security configurations and keeping evidence of completed tasks. Overall, I feel more confident in applying basic cloud security practices.
