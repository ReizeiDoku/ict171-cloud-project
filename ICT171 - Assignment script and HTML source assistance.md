# assignment-documentation.md

# ICT171 Cloud Server Project Documentation

## Student Information

* Name: Jordan Lee
* Student ID: 36059227

## Live Website

* Domain: https://jordanshl.site

## Infrastructure Overview

| Component          | Technology Used         |
| ------------------ | ----------------------- |
| Cloud Provider     | AWS EC2                 |
| Operating System   | Ubuntu Linux            |
| Web Server         | Apache2                 |
| Domain Registrar   | Namecheap               |
| SSL/TLS            | Certbot / Let's Encrypt |
| Scripting Language | Bash                    |
| Website Languages  | HTML / CSS              |

---

# 1. AWS EC2 Ubuntu Server Installation

An Ubuntu Linux EC2 instance was created using Amazon Web Services.

## Security Group Configuration

The following inbound rules were configured:

| Port | Purpose |
| ---- | ------- |
| 22   | SSH     |
| 80   | HTTP    |
| 443  | HTTPS   |

---

# 2. Connecting to the Server

The server was accessed remotely using SSH.

Command used:

```bash
ssh -i key.pem ubuntu@SERVER-IP
```

---

# 3. Updating Ubuntu Packages

The server packages were updated before software installation.

```bash
sudo apt update
sudo apt upgrade -y
```

---

# 4. Apache Web Server Installation

Apache2 was installed to host the website.

```bash
sudo apt install apache2 -y
```

Apache services were started and enabled:

```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

The server was tested using:

```bash
curl http://localhost
```

---

# 5. Basic HTML Website Development

The website files were stored in:

```text
/var/www/html/
```

The main webpage was edited using:

```bash
sudo nano /var/www/html/index.html
```

The website was developed using:

* Basic HTML
* CSS styling

Coding assistance and references were obtained from:

* Codecademy
* W3Schools

These resources assisted with:

* HTML structure
* CSS styling
* Website layout
* Basic web development concepts

---

# 6. DNS Configuration Using Namecheap

The domain name jordanshl.site was purchased through Namecheap.

An A Record was configured to connect the domain to the AWS EC2 public IP address.

DNS Configuration:

```text
Type: A
Host: @
Value: AWS Public IP
```

After DNS propagation, the website became accessible through the domain name.

---

# 7. SSL/TLS Configuration Using Certbot

HTTPS encryption was configured using Certbot and Let's Encrypt.

Certbot installation:

```bash
sudo apt install certbot python3-certbot-apache -y
```

SSL/TLS configuration:

```bash
sudo certbot --apache
```

This generated SSL certificates and enabled HTTPS for the website.

The website is now secured using encrypted HTTPS connections.

---

# 8. Bash Monitoring Script

## server-status.sh

```bash
#!/bin/bash

echo "===== Server Status Report ====="

echo ""
echo "Server Uptime:"
uptime

echo ""
echo "Disk Usage:"
df -h /

echo ""
echo "Memory Usage:"
free -m

echo ""
echo "Apache Status:"
systemctl is-active apache2
```

## Script Explanation

This Bash script retrieves server information including:

* Uptime
* Disk usage
* Memory usage
* Apache service status

The purpose of the script is to demonstrate basic Linux scripting and server monitoring functionality.

---

# 9. Project Outcome

The project successfully demonstrates:

* Infrastructure as a Service deployment
* Linux command-line administration
* Apache web hosting
* DNS configuration
* SSL/TLS security implementation
* Bash scripting
* Technical documentation using GitHub

---

# References

* Codecademy — HTML and CSS guidance
* W3Schools — HTML, CSS, and JavaScript references
* AWS Documentation — EC2 and networking setup
* Certbot Documentation — HTTPS and SSL/TLS configuration
* Apache Documentation — Apache2 configuration guidance
