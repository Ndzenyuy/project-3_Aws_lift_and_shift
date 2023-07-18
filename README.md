# Project_3: AWS lift and shift
In this project, I deployed the architecture of projects 1 & 2 to run on the aws cloud. I built the artifact on my machine using Maven(mvn) and loaded the artifacts to an s3 bucket. The MySql, RabbitMQ and Memchaced were deployed on EC2 instances, running CentOS operating system, inside a security group running in the backend, used Route53 private hosted zone in order for the instances in the backend to communicate using private domain names. The App, an EC2 instance in which tomcat is installed, is configured to load the artifact from S3 tomcat. This instance is placed behind an ELB. In order to obtain high availability, I made an AMI, then lauched an auto scaling group with target tracking to maintain the CPU usage to 60%. Used AWS certificate manager to obtain a certificate in order to access the site through a secure HTTPS connection, attached it to the ELB.

## Architecture
 ![AWS architecture](https://github.com/Ndzenyuy/project-3_Aws_lift_and_shift/blob/main/images/vproject_AWS.jpg)

 ## AWS Services used
   - EC2
   - Route53
   - ELB
   - S3 bucket
   - Amazon Certificates Manager

## Results
![](https://github.com/Ndzenyuy/project-3_Aws_lift_and_shift/blob/main/images/Screenshot%20from%202023-07-13%2012-33-33.png)
![](https://github.com/Ndzenyuy/project-3_Aws_lift_and_shift/blob/main/images/Screenshot%20from%202023-07-13%2012-34-21.png)
![](https://github.com/Ndzenyuy/project-3_Aws_lift_and_shift/blob/main/images/Screenshot%20from%202023-07-13%2012-34-45.png)
![](https://github.com/Ndzenyuy/project-3_Aws_lift_and_shift/blob/main/images/Screenshot%20from%202023-07-13%2012-34-54.png)
![](https://github.com/Ndzenyuy/project-3_Aws_lift_and_shift/blob/main/images/Screenshot%20from%202023-07-13%2012-35-57.png)
