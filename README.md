# Project_3: AWS lift and shift
In this project, I deployed the architecture of projects 1 & 2 to run on the aws cloud. I built the artifact on my machine using Maven(mvn) and loaded the artifacts to an s3 bucket. The MySql, RabbitMQ and Memchaced were deployed on EC2 instances, running CentOS operating system, inside a security group running in the backend, used Route53 private hosted zone in order for the instances in the backend to communicate using private domain names. The App, running on another EC2 instance running tomcat behing an ELB. In order to obtain high availability, I made an AMI, then lauched an auto scaling group with target tracking to maintain the CPU usage to 60%. Used AWS certificate manager to obtain a certificate in order to assess the site through a secure HTTPS connection, attached it to the ELB.

## Architecture


