# Laboratory 08: The Cloud Security Engineer

## Mission Overview

This mission focuses on securing a cloud-based Ubuntu server using the Uncomplicated Firewall (UFW). It demonstrates how to configure firewall rules, manage network access, and protect a running web application.

## Objectives

- Understand the Principle of Least Privilege.
- Identify the attack surface of a virtual machine.
- Understand the Default Deny Policy.
- Deploy and verify an Nginx web application.
- Configure UFW to control incoming and outgoing traffic.
- Allow only the required network ports.

## Commands Executed

### Deploy the Nginx Container

```bash
docker run -d --name secure-web-app -p 8080:80 nginx
docker ps
curl http://localhost:8080
```

### Configure the Firewall

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
```

### Allow Web Application Traffic

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
```

## Skills Learned

- Understanding basic cloud security principles.
- Deploying and testing an Nginx Docker container.
- Configuring UFW firewall rules.
- Applying a Default Deny Policy.
- Managing network ports to reduce the server's attack surface.
- Documenting technical procedures in Markdown.
