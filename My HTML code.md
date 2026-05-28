# progress-report.md

# ICT171 Cloud Server Project Progress Report

## Student Information

* Name: Jordan Lee
* Student ID: 36059227

---

# Project Overview

This project focuses on designing and implementing a cloud-hosted Linux web server using Amazon Web Services EC2. The project demonstrates Infrastructure as a Service deployment, Linux server administration, Apache web hosting, DNS configuration, SSL/TLS implementation, and technical documentation through GitHub.

The project website is accessible through:

* Domain: https://jordanshl.site

---

# Week 6

## Initial Project Planning

* Researched possible cloud server project ideas.
* Selected a cloud-based server deployment and monitoring website project.
* Investigated AWS EC2 virtual machines and Linux server hosting.
* Planned website structure and documentation requirements.

---

# Week 7

## AWS EC2 Deployment

* Created an AWS EC2 Ubuntu Linux instance.
* Configured inbound security group rules:

  * SSH (22)
  * HTTP (80)
  * HTTPS (443)
* Generated SSH key pair for remote access.
* Successfully connected to the server using SSH.

Commands used:

```bash
ssh -i key.pem ubuntu@SERVER-IP
```

---

# Week 8

## Apache Web Server Installation

* Updated Ubuntu packages.
* Installed Apache2 web server software.
* Started and enabled Apache services.
* Tested web server accessibility using the public IP address.

Commands used:

```bash
sudo apt update
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
```

---

# Week 9

## Website Development

* Created initial HTML structure for the project website.
* Added deployment handbook sections.
* Implemented CSS styling for readability and layout.
* Added project overview and server setup instructions.

Resources used:

* Codecademy
* W3Schools

---

# Week 10

## DNS Configuration

* Purchased domain name through Namecheap.
* Configured DNS A record to point toward AWS public IP address.
* Tested DNS propagation and domain accessibility.

DNS record configured:

```text
A Record → AWS Public IP
```

---

# Week 11

## SSL/TLS Configuration

* Installed Certbot and configured HTTPS security.
* Generated SSL/TLS certificates using Let's Encrypt.
* Redirected HTTP traffic to HTTPS.

Commands used:

```bash
sudo apt install certbot python3-certbot-apache -y
sudo certbot --apache
```

---

# Week 12

## Bash Script Development

* Developed a Linux Bash monitoring script.
* Added commands for:

  * Server uptime
  * Disk usage
  * Memory usage
  * Apache status
* Tested script functionality on EC2 instance.

---

# Week 13

## GitHub Documentation

* Organised repository structure.
* Added markdown documentation files.
* Uploaded scripts and screenshots.
* Improved documentation clarity and formatting.

---

# Week 14

## Final Testing and Review

* Tested HTTPS functionality.
* Verified domain accessibility.
* Reviewed documentation completeness.
* Prepared video explainer structure.
* Finalised GitHub repository.

---

# Skills Demonstrated

* AWS EC2 deployment
* Linux server administration
* SSH remote management
* Apache web hosting
* DNS configuration
* SSL/TLS implementation
* Bash scripting
* GitHub documentation
* HTML and CSS development

---

# References

The following resources assisted with research and coding:

* Codecademy — HTML and CSS learning resources
* W3Schools — HTML, CSS, and JavaScript references
* AWS Documentation — EC2 configuration and networking
* Certbot Documentation — SSL/TLS implementation
* Apache Documentation — Apache2 web server configuration
