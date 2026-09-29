# AWS Project 3 – Application Deployment Automation

## Project Overview

This project demonstrates application deployment and basic automation on an AWS Linux EC2 server.

The project uses:

- AWS EC2
- Linux
- Git/GitHub
- Python Flask
- Nginx
- systemd
- Bash scripting
- Amazon S3

The objective is to deploy an application on an EC2 server, configure Nginx as a reverse proxy, manage the application using systemd, automate deployment using a Bash script, and create application backups in Amazon S3.

## Architecture

```text
                    GitHub
                       |
                       v
              +----------------+
              |   AWS EC2      |
              |  Linux Server  |
              +----------------+
                       |
              +--------+--------+
              |                 |
              v                 v
          Nginx             systemd
       Reverse Proxy           |
              |                v
              |          Flask Application
              |                |
              +-------<--------+
                       |
                       v
                    Browser


              Backup Flow
              
          EC2 Application
                |
                v
           backup.sh
                |
                v
          Amazon S3 Bucket
