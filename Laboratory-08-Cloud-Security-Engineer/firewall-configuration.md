# Firewall Configuration

## 1. Allow SSH Access

Command used:

```bash
sudo ufw allow ssh
```

This command allows SSH connections so administrators can remotely manage the server.

## 2. Configure the Default Deny Policy

Commands used:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

These commands block incoming connections by default while allowing outgoing network traffic.

## 3. Activate the Firewall

Command used:

```bash
sudo ufw enable
```

This command activates the firewall and applies the configured security rules.

## 4. Allow Web Application Traffic

Command used:

```bash
sudo ufw allow 8080/tcp
```

This command allows incoming TCP connections through port 8080 so users can access the Nginx web application.

## 5. Verify Firewall Configuration

Commands used:

```bash
sudo ufw status verbose
sudo ufw status numbered
```

These commands display the firewall status, default policies, and configured rules.

## 6. Security Warning

If `sudo ufw enable` is executed before `sudo ufw allow ssh`, SSH connections may be blocked, potentially preventing administrators from remotely accessing the server.
