# Three-Tier WordPress Deployments
## Overview
The aim of this project is to use a custom built Virtual Private Cloud (VPC), a number of Amazon EC2 instances, an Application Load balancing tool, and a private MySQL database to build a WordPress website on Amazon Web Services (AWS).
## Three-Tier Architecture: What Is It?
- An application is divided into three logical levels using a three-tier architecture:
- ``Presentation Tier``: Requests are received and displayed via the user-facing interface.
- ``Application tier``:The application logic that handles requests and interacts with the data tier is known as the application tier.
- ``Data tier``:The database or storage layer that keeps application data is known as the "data tier."

##  Objectives

- Create a unique VPC with private and public subnets.
- Set up NAT Gateway and Internet Gateway routing.
- Set up two front-end WordPress EC2 instances.
- Set up a private EC2 instance for MySQL.
- Set up an application load balancer that faces the internet.
- Use security groups to limit network communication.
- Set up shared storage for uploads from WordPress.
- Record testing, deployment, troubleshooting, and cleaning.
- Use meaningful commits and Git branches to manage project changes.

## Design
### Flow of Requests
This request flow is followed by the application:

User → Internet Gateway → Application Load Balancer → WordPress Frontend EC2 Instances → Private MySQL Database

When necessary, private instances use the NAT Gateway to reach the outside world.
